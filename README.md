<div align="center">

# Krishna Koushik Thokala

### Infrastructure Operations Engineer | AWS · EKS · Terraform · GitOps · Observability

Austin, TX · AWS Certified Solutions Architect – Associate · MS Computer Science, Indiana University Bloomington<br>
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

I build and validate AWS infrastructure around deployment control, measurable reliability, access boundaries, and cost-aware lifecycle management. That approach comes from two years of SLA-driven production NOC operations at Tata Communications, where incident prioritization, restoration commitments, and customer communication were daily responsibilities.

Two operating principles shape the work in these repositories:

**Measure what users experience.** Reliability indicators are scoped to user-facing routes and exclude health, metrics, and load-generation traffic.

**State what the evidence does not prove.** Controlled validation runs publish their limitations alongside their results rather than presenting short tests as production-scale evidence.

**Focus:** Terraform-provisioned AWS foundations · Kubernetes delivery on EKS with Helm and Argo CD · Python automation · Prometheus and CloudWatch observability · incident response · failure and rollback validation

---

## Featured Projects

### [EKS Reliability Platform](https://github.com/krishna310301/cloudops-sre-platform) &nbsp;<sub>`cloudops-sre-platform`</sub>

An EKS reliability-operations platform for service health, deployment history, incident timelines, MTTR, and request-based SLIs, modeled after workflows used in production support.

- Provisioned a **59-resource AWS foundation** with Terraform, including a three-tier VPC, managed EKS, RDS PostgreSQL, ECR, Secrets Manager, IRSA, ALB ingress, and CloudWatch monitoring
- Implemented **6 Prometheus recording rules** and multi-window burn-rate alerts against a 99.9% SLO; verified behavior through **5 promtool cases and 12 assertions**
- Load-tested the Python/FastAPI backend with k6: HPA scaled **2 → 6 replicas across 18,819 requests with zero failed requests or pod restarts**, then returned to baseline
- Published SHA-256-attested validation evidence and verified teardown across 14 service checks, explicitly recording one inconclusive tagging check rather than reporting it as passed

**Tech:** AWS · EKS · Terraform · Helm · Python/FastAPI · Prometheus · RDS PostgreSQL · ECR · IRSA · ALB · CloudWatch · k6 · GitHub Actions · Checkov · kubeconform

**Evidence:** [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Validation Run](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/evidence/aws-validation-2026-07-25) · [SLI Rules](https://github.com/krishna310301/cloudops-sre-platform/blob/main/charts/cloudops-sre-platform/rules/cloudops-sli-rules.yaml) · [Burn-Rate Runbook](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/availability-burn-rate-runbook.md) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture.md)

---

### [GitOps Delivery Platform](https://github.com/krishna310301/cloudops-gitops-platform) &nbsp;<sub>`cloudops-gitops-platform`</sub>

An EKS delivery platform that keeps Git as the source of truth for promotion, drift correction, and rollback.

- Composed the AWS foundation as **15 reusable Terraform modules** for VPC, EKS, ECR, and IAM, with a **$25 monthly AWS Budget** guardrail for the validation environment
- Reconciled **4 Argo CD Applications** across dev, staging, prod, and observability namespaces with scoped RBAC, ResourceQuotas, and Network Policies
- Secured promotion through a **four-gate GitHub Actions workflow** that validates Git and ECR provenance, authenticates through branch-scoped OIDC without stored AWS credentials, and delivers changes through pull requests
- Validated drift self-healing and Git-revert recovery after an injected readiness failure on a live EKS cluster

**Tech:** AWS · EKS · Argo CD · Terraform · Helm · GitHub Actions · OIDC · ECR · Docker · Prometheus · Grafana · AWS Budgets · Kubernetes RBAC

**Evidence:** [Repository](https://github.com/krishna310301/cloudops-gitops-platform) · [AWS Validation](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/aws-validation-results.md) · [Promotion Workflow](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/promotion-workflow.md) · [Rollback Demo](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/rollback-demo.md) · [Drift Detection](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/drift-detection-demo.md)

---

### [Serverless Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor) &nbsp;<sub>`cloudops-uptime-monitor`</sub> — [**live**](https://d3hlcf532b9plq.cloudfront.net)

A deployed Python/Lambda availability monitor with scheduled checks, state history, state-change alerting, and a CloudFront-hosted dashboard.

- Deployed a **53-resource serverless stack** with Lambda, EventBridge, DynamoDB, API Gateway, SNS/SQS, S3, CloudFront, KMS, CloudWatch, X-Ray, and Terraform
- Modeled a latest-status access pattern that reads **10 current rows instead of scanning 86,400 retained records** in the reference workload, holding dashboard-read cost constant as history grows
- Hardened target handling against SSRF and redirect-based time-of-check/time-of-use bypasses; added API throttling, KMS encryption, dead-letter queues, and point-in-time recovery
- Published **9 application-level CloudWatch metrics** and validated stateful alerting through an outage drill with **1-second detection, 26-second dashboard visibility, and zero duplicate DOWN alerts**

**Tech:** AWS · Python · Lambda · DynamoDB · API Gateway · EventBridge · SNS/SQS · S3 · CloudFront · KMS · X-Ray · CloudWatch · Terraform · GitHub Actions · Bandit · Checkov

**Evidence:** [Live Dashboard](https://d3hlcf532b9plq.cloudfront.net) · [Repository](https://github.com/krishna310301/cloudops-uptime-monitor) · [Failure Drill](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/failure-drill.md) · [Design Tradeoffs](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/design-tradeoffs.md) · [Security Notes](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/security.md)

---

## Additional Project

### [AWS Incident Triage Pipeline](https://github.com/krishna310301/aws-incident-triage-pipeline)

An event-driven incident-response workflow in which CloudWatch and SNS invoke a Python Lambda that assigns deterministic severity, generates remediation-focused summaries through Bedrock, and falls back to structured notifications when model output is unavailable. Terraform provisions the workflow; GitHub Actions runs Python unit tests, Bandit, Checkov, and IaC validation.

---

## Technical Stack

| Area | Tools |
|---|---|
| **AWS** | EC2, VPC, EKS, ECR, Lambda, API Gateway, RDS, DynamoDB, S3, CloudFront, SNS, SQS, EventBridge, KMS, Secrets Manager, IAM, ALB, NAT Gateway, CloudWatch, X-Ray, Budgets |
| **IaC & Delivery** | Terraform modules and lifecycle, Helm, Kubernetes, Docker, Argo CD, GitOps, GitHub Actions, CI/CD, AWS CLI, Checkov, kubeconform |
| **Security & Access** | IAM roles and policies, IRSA, OIDC federation, RBAC, Pod Security, Network Policies, KMS encryption, secrets management, SSRF input validation |
| **Observability** | Prometheus, Grafana, CloudWatch Logs/Alarms/Dashboards, recording rules, SLIs/SLOs, burn-rate alerting, HPA, X-Ray, k6 |
| **Systems & Networking** | Linux, TCP/IP, HTTP/S, DNS, BGP, MPLS, DWDM, subnetting, routing, load balancing, firewalls |
| **Languages & Data** | Python, Bash, SQL, PostgreSQL, DynamoDB, FastAPI, Git |

---

## Production Operations Background

### Tata Communications — Senior Engineer, Network Operations Center (Shift Lead)
*July 2022 – July 2024 · Pune, India*

- Led five-engineer shifts in a 24/7 carrier NOC, coordinating triage for **40+ daily incidents across 25–30 Tier-1 clients** and prioritizing concurrent P1/P2 outages against 99.9% availability and four-hour restoration commitments
- Diagnosed BGP/MPLS routing failures, TCP/IP faults, DWDM impairments, and hardware failures across Juniper, Huawei, Ciena, and Alcatel infrastructure
- Directed incident restoration through ServiceNow, coordinating vendor TAC escalation, field dispatch, customer-premises testing, and client communication
- Produced post-incident RCAs and cross-shift handoffs that preserved diagnostic context and supported recurrence prevention; earned a **Certificate of Excellence** for resolving an escalated customer incident

---

## Education and Certification

- **[AWS Certified Solutions Architect – Associate](https://www.credly.com/badges/97f0c690-8ec1-4a22-b1d1-7d33ae91a1c5/public_url)** — Amazon Web Services, July 2026
- **MS, Computer Science** — Indiana University Bloomington, May 2026
- **B.Tech, Computer Science and Engineering** — SRM Institute of Science and Technology, 2022

---

<div align="center">
<sub>Every quantitative claim above links to supporting code, test results, or validation evidence.</sub>
</div>
