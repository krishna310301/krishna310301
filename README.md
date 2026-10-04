<div align="center">

# Krishna Koushik Thokala

### Infrastructure Engineer | AWS · Kubernetes · Terraform · GitOps · Observability

Austin, TX · AWS Certified Solutions Architect – Associate · MS Computer Science, Indiana University Bloomington  
2+ years of production network operations experience supporting Tier-1 carrier infrastructure

<p>
  <a href="https://linkedin.com/in/krishna3103">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="https://krishna310301.github.io">Portfolio</a>
  &nbsp;·&nbsp;
  <a href="https://krishna310301.github.io/assets/Krishna_Koushik_Resume.pdf">Resume</a>
  &nbsp;·&nbsp;
  <a href="https://www.credly.com/badges/97f0c690-8ec1-4a22-b1d1-7d33ae91a1c5/public_url">AWS Credential</a>
  &nbsp;·&nbsp;
  <a href="mailto:krishnakoushikthokala@gmail.com">Email</a>
</p>

</div>

---

## About

I am an infrastructure engineer with 2+ years of production network operations experience in 24/7 Tier-1 carrier environments, including incident response, change execution, root cause analysis, and SLA-driven restoration.

I now apply that operations foundation to hands-on AWS infrastructure: Terraform-managed EKS and serverless systems, GitOps/CI/CD delivery, Python automation, and Prometheus/CloudWatch observability.

My projects emphasize two principles:

**Measure what users experience.** Reliability indicators should represent meaningful application behavior rather than simply proving that infrastructure exists.

**State what the evidence proves.** Validation runs document their scope and limitations instead of presenting short-lived tests as production-scale results.

**Core stack:** AWS · Terraform · Kubernetes · Docker · Helm · Argo CD · GitHub Actions · Python · Linux · Prometheus · Grafana · CloudWatch

---

## Featured Projects

### [EKS Reliability Platform](https://github.com/krishna310301/cloudops-sre-platform)

Reliability-operations platform deployed on AWS EKS for service health, incidents, deployments, MTTR, SLOs, and error budgets.

- Provisioned the AWS foundation with **Terraform**, including VPC networking, EKS, ECR, private RDS PostgreSQL, IAM, Secrets Manager, and CloudWatch
- Implemented request-based availability and latency SLIs with **Prometheus** and multi-window burn-rate alerts against a **99.9% SLO**, with rule behavior tested in CI
- Validated HPA elasticity with **18,819 k6 requests**: the backend scaled **2 → 6 → 2 replicas with zero request failures and zero pod restarts**
- Documented deployment, observability, validation, teardown, and known limitations as reproducible engineering evidence

**Tech:** AWS · EKS · Terraform · Helm · Python/FastAPI · Prometheus · Grafana · RDS · ECR · CloudWatch · k6 · GitHub Actions

**Explore:** [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Validation Evidence](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/evidence/aws-validation-2026-07-25) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture.md) · [Results](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/results.md)

---

### [GitOps Delivery Platform](https://github.com/krishna310301/cloudops-gitops-platform)

EKS delivery platform using Git as the source of truth for environment promotion, reconciliation, and recovery.

- Built GitOps delivery across **dev, staging, and prod** using Argo CD, Helm, EKS, ECR, Terraform, and GitHub Actions
- Used **GitHub OIDC** and immutable ECR images for promotion without storing long-lived AWS credentials
- Applied namespace-scoped **RBAC, ResourceQuotas, and NetworkPolicies** to define environment boundaries
- Validated Argo CD self-healing after manual replica drift and restored a deliberately broken staging release through **Git revert**

**Tech:** AWS · EKS · Argo CD · Terraform · Helm · GitHub Actions · OIDC · ECR · Docker · Prometheus · Grafana

**Explore:** [Repository](https://github.com/krishna310301/cloudops-gitops-platform) · [AWS Validation](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/aws-validation-results.md) · [Promotion Workflow](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/promotion-workflow.md) · [Rollback Demo](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/rollback-demo.md)

---

### [Serverless Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor) — [**Live Dashboard**](https://d3hlcf532b9plq.cloudfront.net)

Serverless AWS availability monitor with scheduled checks, state-change alerting, retained history, observability, and a live dashboard.

- Built the platform with **Lambda, EventBridge, DynamoDB, API Gateway, SNS, CloudWatch, CloudFront, and Terraform**
- Redesigned latest-status access to read **10 current-state records instead of scanning 86,400 retained records** for the documented 10-URL/30-day reference workload
- Hardened outbound URL checks against **SSRF**, including unsafe DNS resolution and redirect destinations
- Validated the complete outage path in AWS: **1-second observed failure detection, DOWN visible on the dashboard within 26 seconds, no duplicate DOWN alert on the repeated failure check, and verified recovery notification**

**Tech:** AWS · Python · Lambda · DynamoDB · EventBridge · API Gateway · SNS · CloudWatch · CloudFront · Terraform · GitHub Actions

**Explore:** [Live Dashboard](https://d3hlcf532b9plq.cloudfront.net) · [Repository](https://github.com/krishna310301/cloudops-uptime-monitor) · [Failure Drill](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/failure-drill.md) · [Engineering Metrics](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/metrics.md)

---

## Additional Project

### [AWS Incident Triage Pipeline](https://github.com/krishna310301/aws-incident-triage-pipeline)

Python/AWS incident-response workflow that processes CloudWatch alarms through Lambda, assigns deterministic severity, generates remediation-focused summaries with Amazon Bedrock, and falls back to structured notifications when AI output is unavailable.

**Tech:** Python · Lambda · CloudWatch · SNS · Bedrock · Terraform · GitHub Actions

---

## Production Operations Background

### Tata Communications — Senior Engineer, Network Operations Center · Shift Lead
*July 2022 – July 2024 · Pune, India*

- Led five-engineer shifts in a 24/7 NOC, prioritizing **40+ daily incidents across 25+ Tier-1 carrier clients** while supporting 99.9% availability targets and four-hour restoration SLAs
- Led P1/P2 incident response across BGP/MPLS, TCP/IP, DNS, DWDM, and hardware faults while coordinating vendor TAC, field teams, customer testing, and client communication
- Executed planned network changes with pre/post validation and rollback procedures
- Authored runbooks, post-incident RCAs, and standardized shift handoffs; earned a **Certificate of Excellence** for resolving an escalated customer case

---

## Technical Toolkit

| Area | Technologies |
|---|---|
| **Cloud & IaC** | AWS, Terraform, VPC, EC2, EKS, Lambda, RDS, DynamoDB, S3, IAM |
| **Containers & Delivery** | Kubernetes, Docker, Helm, Argo CD, GitHub Actions, GitOps, CI/CD, ECR |
| **Observability & Reliability** | Prometheus, Grafana, CloudWatch, SLIs/SLOs, burn-rate alerting, k6 |
| **Systems & Automation** | Linux, Python, Bash, Git, SQL |
| **Networking & Security** | TCP/IP, DNS, BGP, MPLS, OIDC, RBAC, NetworkPolicies, Secrets Manager |

---

## Education & Certification

- **[AWS Certified Solutions Architect – Associate](https://www.credly.com/badges/97f0c690-8ec1-4a22-b1d1-7d33ae91a1c5/public_url)** — Amazon Web Services, 2026
- **MS, Computer Science** — Indiana University Bloomington, 2026
- **B.Tech, Computer Science and Engineering** — SRM Institute of Science and Technology, 2022

---

<div align="center">
<sub>Project repositories include architecture notes, validation records, runbooks, and documented tradeoffs.</sub>
</div>
