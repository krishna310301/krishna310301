<div align="center">

# Krishna Koushik Thokala

### Cloud Infrastructure Engineer | AWS · EKS · Terraform · GitOps · Observability

AWS Certified Solutions Architect – Associate · MS Computer Science, Indiana University Bloomington
2 years of production NOC operations supporting Tier-1 carrier infrastructure

<p>
  <a href="https://linkedin.com/in/krishna3103">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="https://krishna310301.github.io">Portfolio</a>
  &nbsp;·&nbsp;
  <a href="https://krishna310301.github.io/assets/Krishna_Koushik_Resume.pdf">Resume</a>
  &nbsp;·&nbsp;
  <a href="https://d3hlcf532b9plq.cloudfront.net">Live Dashboard</a>
  &nbsp;·&nbsp;
  <a href="https://www.credly.com/badges/97f0c690-8ec1-4a22-b1d1-7d33ae91a1c5/public_url">AWS Credential</a>
  &nbsp;·&nbsp;
  <a href="mailto:krishnakoushikthokala@gmail.com">Email</a>
</p>

</div>

---

## Engineering Focus

I build AWS infrastructure around deployment control, measurable reliability, access boundaries, and cost-aware lifecycle management. The approach comes from two years of SLA-driven production NOC operations at Tata Communications, where incidents were real and restoration windows were contractual.

Two habits carry over from that work and show up in every repository here:

**Measure what users experience, not what dashboards display.** Availability indicators are scoped to user-facing routes and exclude health, metrics, and load-generation traffic, because including your own synthetic traffic inflates the number you are trying to trust.

**Record what the evidence does not prove.** Validation runs here publish their own limitations alongside their results. A short controlled run does not establish production capacity, and saying so is part of the artifact.

Focus areas: Terraform-provisioned AWS foundations · Kubernetes delivery on EKS with Helm and Argo CD · Prometheus and CloudWatch observability · incident response, failure drills, and rollback validation · short-lived environments with verified teardown

---

## Featured Projects

### [EKS Reliability Platform](https://github.com/krishna310301/cloudops-sre-platform) &nbsp;<sub>`cloudops-sre-platform`</sub>

An SRE operations platform on Amazon EKS covering service health, deployment history, incident timelines, MTTR, and request-based reliability indicators — built to model the workflows I ran during production support.

- Provisioned a **59-resource** AWS foundation with Terraform: VPC across public, private, and database subnet tiers, EKS cluster with managed node group and OIDC provider, RDS PostgreSQL, ECR, Secrets Manager, IRSA role for the AWS Load Balancer Controller, and CloudWatch log groups and alarms
- Defined availability and latency SLIs as **6 Prometheus recording rules** across 5m, 30m, 1h, and 6h windows, scoped to user-facing routes and counting only 5xx as failure, so client validation errors are not recorded as unavailability
- Alerted on **multi-window, multi-burn-rate** error budget consumption against a 99.9% target — 14.4× fast burn on paired 5m/1h windows paging, 6× slow burn on 30m/6h windows ticketing, each gated on non-zero eligible traffic and routed to a written runbook
- Verified rule correctness with **5 promtool test cases and 12 assertions**, including namespace and service cardinality isolation and the 4xx-vs-5xx classification boundary
- Validated HPA under k6 load: backend scaled **2 → 6 replicas at 496% CPU across 18,819 requests with zero failed requests and zero pod restarts**, then returned to baseline (p50 762ms, p95 1.94s)
- Ran the full validation in a short-lived environment, **destroyed it 54 minutes after apply**, and confirmed closure across 14 checks — 13 passed, with the resource-tagging check explicitly recorded as *inconclusive* rather than passed, because the AWS Resource Groups Tagging API returns previously-tagged resources
- Published **SHA-256-attested evidence artifacts** with a manifest, so every figure above is traceable to a file in this repository

**Tech:** EKS · Terraform · Helm · Prometheus · RDS PostgreSQL · ECR · Secrets Manager · ALB Ingress · CloudWatch · k6 · GitHub Actions · Checkov · kubeconform · FastAPI · React

**Links:** [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Validation Evidence](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/evidence/aws-validation-2026-07-25) · [SLI Rules](https://github.com/krishna310301/cloudops-sre-platform/blob/main/charts/cloudops-sre-platform/rules/cloudops-sli-rules.yaml) · [Burn-Rate Runbook](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/availability-burn-rate-runbook.md) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture.md)

---

### [GitOps Delivery Platform](https://github.com/krishna310301/cloudops-gitops-platform) &nbsp;<sub>`cloudops-gitops-platform`</sub>

A Git-as-source-of-truth delivery platform on EKS — built to validate how Kubernetes changes move between environments, how Argo CD detects and corrects drift, and how a failed release recovers through Git alone.

- Composed the AWS foundation as **15 reusable Terraform modules** provisioning VPC, EKS, ECR, and IAM, under a **$25 monthly AWS Budget** guardrail scoped to the short-lived validation environment
- Ran **4 Argo CD Applications** across `dev`, `staging`, `prod`, and `observability` namespaces under 2 AppProjects, each namespace isolated by scoped RBAC, NetworkPolicies, and ResourceQuotas
- Built a **four-gate promotion pipeline**: the workflow rejects any tag that is not a verified 12-character commit SHA, confirms the commit exists in Git via `git cat-file`, confirms the image exists in ECR via `describe-images`, authenticates through a branch-scoped GitHub OIDC role with no stored AWS credentials, and lands every promotion as a reviewable pull request
- Validated **drift self-healing and Git-revert recovery** after an injected readiness failure on a live EKS cluster, then tore down all 20 Terraform-managed resources
- Brought all Applications to `Synced` and `Healthy`, with workloads observed through Prometheus and Grafana

**Tech:** EKS · Argo CD · Terraform (modules) · Helm · GitHub Actions · GitHub OIDC · ECR · Docker · Prometheus · Grafana · AWS Budgets · Kubernetes RBAC · NetworkPolicies · ResourceQuotas

**Links:** [Repository](https://github.com/krishna310301/cloudops-gitops-platform) · [AWS Validation Results](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/aws-validation-results.md) · [Promotion Workflow](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/promotion-workflow.md) · [Rollback Demo](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/rollback-demo.md) · [Drift Detection](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/drift-detection-demo.md)

---

### [Serverless Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor) &nbsp;<sub>`cloudops-uptime-monitor`</sub> — [**live**](https://d3hlcf532b9plq.cloudfront.net)

A serverless availability monitor that checks target URLs on a schedule, stores current and historical status, sends state-change alerts, and serves a React dashboard through CloudFront. **This one is deployed and running.**

- Designed a **53-resource** serverless stack: EventBridge-scheduled Lambda checks, DynamoDB status history with TTL retention and point-in-time recovery, SNS alerting, API Gateway with request validation, usage plans, API keys, and throttling, and a CloudFront/S3 dashboard served through Origin Access Control
- Modeled a **dedicated latest-status access pattern** so dashboard refreshes read 10 current rows instead of scanning 86,400 retained records in the 10-URL, 30-day reference workload, holding read cost flat as retention grows
- Built a **stateful alerting engine** that distinguishes `UP → DOWN`, `DOWN → DOWN`, and `DOWN → UP` transitions, so sustained outages do not generate repeat pages while recovery notifications still fire
- Hardened user-submitted targets against **SSRF**: loopback, private RFC1918, link-local, reserved, and EC2 instance-metadata addresses are rejected, and targets are **revalidated after DNS resolution before redirects are followed**, closing the time-of-check-to-time-of-use gap that defeats static denylists
- Encrypted DynamoDB, SQS, and S3 with a **customer-managed KMS key**, and routed both Lambdas to dead-letter queues with 14-day retention
- Published **6 custom CloudWatch metrics** (`URLsChecked`, `URLsDown`, `AlertsSent`, `URLCheckLatencyMs`, `CheckRunDurationMs`, `MonitoredURLCount`) alongside a dashboard and 4 metric alarms
- Completed a **documented outage drill**: failure injected at `23:51:14Z`, stored as DOWN at `23:51:15Z` (1-second detection), dashboard reflected DOWN at `23:51:41Z`, repeat check deduplicated with no second alert, recovery confirmed and notified at `23:52:37Z`

**Tech:** Lambda · DynamoDB · API Gateway · EventBridge · SNS · SQS · S3 · CloudFront · KMS · X-Ray · CloudWatch · Terraform · Checkov · GitHub Actions · React

**Links:** [Live Dashboard](https://d3hlcf532b9plq.cloudfront.net) · [Repository](https://github.com/krishna310301/cloudops-uptime-monitor) · [Failure Drill](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/failure-drill.md) · [Design Tradeoffs](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/design-tradeoffs.md) · [Security Notes](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/security.md)

---

## Technical Stack

| Area | Tools |
|---|---|
| **AWS** | EC2, VPC, EKS, ECR, Lambda, API Gateway, RDS, DynamoDB, S3, CloudFront, SNS, SQS, EventBridge, KMS, Secrets Manager, IAM, ALB, NAT Gateway, CloudWatch, X-Ray, Budgets |
| **IaC & Delivery** | Terraform (modules, remote state, plan/apply/destroy lifecycle), Helm, Kubernetes, Docker, Argo CD, GitOps, GitHub Actions, CI/CD, Checkov, kubeconform |
| **Security & Access** | IAM roles and policies, IRSA, OIDC federation, RBAC, Pod Security, NetworkPolicies, KMS encryption, Secrets management, SSRF input validation |
| **Observability** | Prometheus, Grafana, CloudWatch (Logs, Alarms, Dashboards, Container Insights), recording rules, SLIs, burn-rate alerting, HPA, k6 |
| **Networking** | BGP, MPLS, TCP/IP, DNS, DWDM, subnetting, routing, load balancing, firewalls |
| **Languages & Platforms** | Python, Bash, SQL, PostgreSQL, Linux, Git, ServiceNow, FastAPI, React |

---

## Production Operations Background

### Tata Communications — Senior Engineer, Network Operations Center (Shift Lead)
*July 2022 – July 2024 · Pune, India*

Ran 24/7 production NOC operations for 25–30 Tier-1 carrier clients across global ILL, DWDM, and submarine cable networks.

- Led 5-engineer shifts handling **40+ daily priority incidents**, owning triage, escalation, and restoration end to end
- Diagnosed BGP/MPLS routing failures, TCP/IP connectivity faults, DWDM impairments, and hardware failures across **Juniper, Huawei, Ciena, and Alcatel** platforms
- Coordinated vendor TAC engagement, field dispatch, and customer-premises testing through to resolution
- Prioritized concurrent P1/P2 incidents in ServiceNow against **99.9% availability and 4-hour restoration commitments**, maintaining direct customer communication throughout active outages
- Authored post-incident RCAs and structured shift handoffs that preserved troubleshooting context across rotations
- Earned a **Certificate of Excellence** for resolving an escalated incident into a documented customer win

---

## Education and Certifications

- **[AWS Certified Solutions Architect – Associate](https://www.credly.com/badges/97f0c690-8ec1-4a22-b1d1-7d33ae91a1c5/public_url)** — Amazon Web Services, 2026
- **MS, Computer Science** — Indiana University Bloomington, May 2026
- **B.Tech, Computer Science and Engineering** — SRM Institute of Science and Technology, 2022

---

<div align="center">
<sub>Every figure on this page is traceable to an artifact in the linked repository.</sub>
</div>
