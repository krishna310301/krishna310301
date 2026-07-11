<div align="center">

# Krishna Koushik Thokala

### Cloud Infrastructure Engineer | AWS, EKS, Terraform, GitOps, Observability

AWS Certified Solutions Architect - Associate · MS Computer Science, Indiana University Bloomington  
2+ years production NOC operations experience supporting Tier-1 carrier infrastructure

<p>
  <a href="https://linkedin.com/in/krishna3103">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="mailto:krishnakoushikthokala@gmail.com">krishnakoushikthokala@gmail.com</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/krishna310301">GitHub</a>
  &nbsp;·&nbsp;
  <a href="https://krishna310301.github.io">Portfolio</a>
</p>

</div>

---

## Engineering Focus

I build AWS infrastructure projects around deployment control, observability, failure recovery, access boundaries, and cost-aware infrastructure lifecycle management.

Before moving deeper into cloud infrastructure, I worked in 24/7 production NOC operations at Tata Communications, supporting SLA-driven incident response for Tier-1 carrier clients. That work shaped how I approach cloud systems: clear ownership, reliable runbooks, observable services, and clean rollback paths.

Focus:

- AWS infrastructure with Terraform
- Kubernetes workloads on Amazon EKS
- GitOps delivery with Argo CD and Helm
- CI/CD with GitHub Actions
- Observability with Prometheus, Grafana, and CloudWatch
- SRE workflows, incident response, and rollback validation

Operations background:

- 2+ years production network operations
- 25-30 Tier-1 carrier clients
- SLA-driven triage, escalation, RCA, and service restoration
- BGP, MPLS, TCP/IP, DWDM, and segment-wise fault isolation

---

## Featured Projects

### [CloudOps GitOps Platform](https://github.com/krishna310301/cloudops-gitops-platform)

EKS GitOps delivery platform using Argo CD, Helm, Terraform, GitHub Actions, ECR, Prometheus, Grafana, and AWS Budgets.

Built to validate how Kubernetes changes move through Git-managed environments, how Argo CD detects drift, how failed releases recover through Git, and how AWS validation environments are managed with cost controls.

Implemented:

- Argo CD AppProjects and multi-source Applications for `dev`, `staging`, `prod`, and `observability`
- Git-managed Helm values for namespace-isolated dev/staging/prod environments
- Terraform-managed AWS foundation across VPC, EKS, ECR, IAM, and AWS Budgets
- ResourceQuotas, scoped RBAC, ServiceAccounts, probes, resource limits, and hardened pod security settings
- GitHub Actions workflows for tests, manifest validation, immutable commit-SHA image publishing, and PR-based environment promotion
- Repository-scoped GitHub OIDC role for ECR publishing without long-lived AWS access keys
- Drift self-healing after manual replica changes
- Git revert rollback after a Helm-controlled readiness failure
- Argo CD-managed Prometheus/Grafana observability with app ServiceMonitor targets
- Same-day Terraform destroy with empty state, AWS resource checks, and project tag sweep

Run results:

- 20 AWS resources created and destroyed with Terraform
- 4 Argo CD Applications reached `Synced` and `Healthy` on real EKS
- Prometheus scraped app metrics across dev/staging/prod
- Grafana dashboard captured workload health, replicas, CPU, memory, request rate, and app health
- ECR image tags validated for all environments
- AWS Budget created through Terraform and removed during cleanup

Tech: EKS, Argo CD, Helm, Terraform, GitHub Actions, ECR, Docker, Prometheus, Grafana, AWS Budgets, Kubernetes RBAC

Links: [Repository](https://github.com/krishna310301/cloudops-gitops-platform) · [Validation Output](https://github.com/krishna310301/cloudops-gitops-platform/tree/main/docs/screenshots) · [AWS Results](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/aws-validation-results.md)

---

### [CloudOps SRE Platform](https://github.com/krishna310301/cloudops-sre-platform)

EKS SRE operations platform for service health, deployment history, incident timelines, MTTR, and simplified SLO-style reliability views.

Built to model the workflows used during production support: service ownership, incident state, deployment visibility, reliability metrics, and validation under load.

Implemented:

- React and FastAPI workloads deployed behind ALB Ingress on Amazon EKS
- Helm-managed Kubernetes deployments, services, resource limits, liveness/readiness probes, and Secrets Manager-backed database credentials
- Terraform-managed AWS infrastructure across VPC, EKS, ECR, RDS PostgreSQL, IAM, Secrets Manager, security groups, and CloudWatch
- Service catalog, incident workflow, deployment history, MTTR calculation, and simplified error-budget views
- Structured logging, request correlation IDs, Alembic migrations, backend unit tests, frontend and container builds, Helm lint, Kubernetes schema validation, Terraform format/validate, cost guardrails, and advisory Checkov scanning
- AWS validation run with screenshots and same-day Terraform destroy

Run results:

- HPA scaled backend replicas from 2 to 6 under k6 load
- Processed 2,035 requests at a 99.5% success rate
- Measured 1.52s p95 latency
- Confirmed scaling through HPA status and CloudWatch logs

Tech: EKS, Kubernetes, Helm, Terraform, Docker, ECR, RDS PostgreSQL, ALB Ingress, CloudWatch, GitHub Actions, FastAPI, React

Links: [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Run Screenshots](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/screenshots/aws-demo-2026-06-06) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture/cloudops-sre-platform-architecture.png)

---

### [CloudOps Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor)

Serverless uptime monitoring platform that checks website availability, stores current and historical status, sends state-change alerts, and serves a React dashboard through CloudFront.

Implemented:

- EventBridge-scheduled Lambda checks every 5 minutes
- DynamoDB status history and latest-status access pattern
- Public read-only dashboard routes with API Gateway key-based quotas, throttling, GET-only CORS, and request validation
- SNS downtime and recovery alerts with state-change suppression
- KMS encryption, DLQs, X-Ray tracing, access logs, CloudWatch dashboards, and log retention
- GitHub Actions validation for Lambda tests, React build, Terraform validation, Bandit, Checkov, S3 sync, and CloudFront invalidation

Run results:

- Designed a latest-status access pattern that reads 10 current-state rows instead of scanning up to 86,400 monthly history rows for a 10-URL reference workload
- Published 9 custom CloudWatch metrics
- Hardened URL intake with unsafe target blocking and redirect validation
- A controlled outage drill detected failure in 1 second, showed the DOWN state within 26 seconds, suppressed duplicate DOWN alerts, and confirmed recovery

Tech: Lambda, DynamoDB, API Gateway, EventBridge, SNS, S3, CloudFront, CloudWatch, Terraform, React, GitHub Actions, IAM, KMS, X-Ray

Links: [Repository](https://github.com/krishna310301/cloudops-uptime-monitor) · [Failure Drill](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/failure-drill.md)

---

## Technical Stack

| Area | Tools |
|---|---|
| Cloud | AWS, VPC, IAM, EC2, S3, Lambda, API Gateway, EventBridge, DynamoDB, RDS, EKS, ECR, ALB, CloudFront, SNS, Secrets Manager, CloudWatch, KMS, AWS Budgets |
| Infrastructure | Terraform, Docker, Kubernetes, Helm, Argo CD, GitOps, GitHub Actions, Linux, Bash |
| Observability and SRE | Prometheus, Grafana, CloudWatch Logs/Metrics/Alarms, HPA, k6, incident response, RCA, runbooks, SLO/SLA, MTTR |
| Networking | TCP/IP, DNS, BGP, MPLS, VPN, load balancing, firewalls, network security, DWDM |
| Programming | Python, SQL, PostgreSQL, REST APIs, FastAPI, React |

---

## Production Operations Background

### Tata Communications - Senior Engineer, Shift Lead

Supported 24/7 production NOC operations for 25-30 Tier-1 carrier clients across global ILL, DWDM, and submarine cable networks.

- Led incident triage, escalation, TAC/vendor coordination, field dispatch, customer-premises testing, and service restoration
- Diagnosed BGP/MPLS routing failures, TCP/IP connectivity issues, DWDM faults, and equipment failures across Juniper, Huawei, Ciena, and Alcatel platforms
- Led 5-person shifts handling 40+ daily priority incidents and escalations
- Created RCA notes, structured handoffs, and cross-functional follow-up through resolution
- Supported 99.9% annual network availability and restored high-priority services within 4-hour SLA targets
- Earned Certificate of Excellence

---

## Education and Certifications

- AWS Certified Solutions Architect - Associate, 2026
- MS Computer Science, Indiana University Bloomington, May 2026
- B.Tech Computer Science and Engineering, SRM Institute of Science and Technology

---

## GitHub Activity

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=krishna310301&theme=tokyonight&hide_border=true&background=0d1117&ring=38BDF8&fire=0EA5E9&currStreakLabel=38BDF8&sideLabels=CBD5E1&dates=94A3B8)](https://github.com/krishna310301)

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=krishna310301&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=38BDF8&line=0EA5E9&point=ffffff)](https://github.com/krishna310301)

</div>
