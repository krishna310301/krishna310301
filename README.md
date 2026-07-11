<div align="center">

# Krishna Koushik Thokala

### Cloud Infrastructure Engineer | AWS, EKS, Terraform, GitOps, Observability

AWS Certified Solutions Architect - Associate · MS Computer Science, Indiana University Bloomington  
2+ years production NOC operations experience supporting Tier-1 carrier infrastructure

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

## Engineering Focus

I build AWS infrastructure projects around deployment control, observability, failure recovery, access boundaries, and cost-aware lifecycle management. My approach is grounded in 2+ years of SLA-driven production NOC operations at Tata Communications.

Focus:

- AWS infrastructure with Terraform and GitHub Actions
- Kubernetes delivery on Amazon EKS with Helm and Argo CD
- Observability with CloudWatch, Prometheus, and Grafana
- Incident response, failure recovery, and rollback validation

---

## Featured Projects

### [CloudOps GitOps Platform](https://github.com/krishna310301/cloudops-gitops-platform)

EKS GitOps delivery platform using Argo CD, Helm, Terraform, GitHub Actions, ECR, Prometheus, Grafana, and AWS Budgets.

Built to validate how Kubernetes changes move through Git-managed environments, how Argo CD detects drift, how failed releases recover through Git, and how AWS validation environments are managed with cost controls.

- Managed `dev`, `staging`, `prod`, and observability through Argo CD multi-source Applications and Git-managed Helm values
- Added namespace quotas, scoped RBAC, NetworkPolicies, hardened pod settings, commit-SHA image validation, and a repository-scoped GitHub OIDC role definition
- Validated drift self-healing and Git-revert recovery after a readiness failure on a short-lived EKS environment
- Brought 4 Argo CD Applications to `Synced` and `Healthy`, observed workloads with Prometheus/Grafana, and destroyed 20 Terraform-managed AWS resources after validation

Tech: EKS, Argo CD, Helm, Terraform, GitHub Actions, ECR, Docker, Prometheus, Grafana, AWS Budgets, Kubernetes RBAC

Links: [Repository](https://github.com/krishna310301/cloudops-gitops-platform) · [Validation Output](https://github.com/krishna310301/cloudops-gitops-platform/tree/main/docs/screenshots) · [AWS Results](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/aws-validation-results.md)

---

### [CloudOps SRE Platform](https://github.com/krishna310301/cloudops-sre-platform)

EKS SRE operations platform for service health, deployment history, incident timelines, MTTR, and simplified SLO-style reliability views.

Built to model the workflows used during production support: service ownership, incident state, deployment visibility, reliability metrics, and validation under load.

- Deployed React and FastAPI workloads behind ALB Ingress with Helm, probes, resource limits, RDS PostgreSQL, and Secrets Manager-backed credentials
- Provisioned VPC, EKS, ECR, RDS, IAM, security groups, and CloudWatch integration with Terraform
- Implemented service, deployment, incident, MTTR, and simplified SLO-style reliability views with structured logs and request IDs
- Validated HPA scale-out from 2 to 6 backend pods under k6 load: 2,035 requests, 99.5% success, and 1.52s p95 latency

Tech: EKS, Kubernetes, Helm, Terraform, Docker, ECR, RDS PostgreSQL, ALB Ingress, CloudWatch, GitHub Actions, FastAPI, React

Links: [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Run Screenshots](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/screenshots/aws-demo-2026-06-06) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture/cloudops-sre-platform-architecture.png)

---

### [CloudOps Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor)

Serverless uptime monitoring platform that checks website availability, stores current and historical status, sends state-change alerts, and serves a React dashboard through CloudFront.

- Scheduled Lambda checks with EventBridge, stored history and current state in DynamoDB, and sent state-change alerts through SNS
- Added API keys, quotas, throttling, restricted CORS, KMS, DLQs, X-Ray, unsafe-target blocking, and redirect validation
- Designed a latest-status access pattern that reduces candidate records from 86,400 history rows to 10 current-state rows for a 10-URL, 30-day reference workload
- Published 9 CloudWatch metrics and completed an outage drill with 1-second detection, 26-second dashboard visibility, recovery notification, and no duplicate DOWN alerts

Tech: Lambda, DynamoDB, API Gateway, EventBridge, SNS, S3, CloudFront, CloudWatch, Terraform, React, GitHub Actions, IAM, KMS, X-Ray

Links: [Repository](https://github.com/krishna310301/cloudops-uptime-monitor) · [Live Dashboard](https://d3hlcf532b9plq.cloudfront.net) · [Failure Drill](https://github.com/krishna310301/cloudops-uptime-monitor/blob/main/docs/failure-drill.md)

---

## Technical Stack

| Area | Tools |
|---|---|
| Cloud | AWS, VPC, IAM, EKS, ECR, RDS, Lambda, DynamoDB, CloudWatch |
| Infrastructure | Terraform, Docker, Kubernetes, Helm, Argo CD, GitHub Actions |
| Reliability | HPA, probes, structured logging, alerting, k6, incident response, RCA, runbooks |
| Networking | TCP/IP, DNS, BGP, MPLS, load balancing, firewalls, DWDM |
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

- [AWS Certified Solutions Architect - Associate](https://www.credly.com/badges/97f0c690-8ec1-4a22-b1d1-7d33ae91a1c5/public_url), 2026
- MS Computer Science, Indiana University Bloomington, May 2026
- B.Tech Computer Science and Engineering, SRM Institute of Science and Technology

---

## GitHub Activity

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=krishna310301&theme=tokyonight&hide_border=true&background=0d1117&ring=38BDF8&fire=0EA5E9&currStreakLabel=38BDF8&sideLabels=CBD5E1&dates=94A3B8)](https://github.com/krishna310301)

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=krishna310301&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=38BDF8&line=0EA5E9&point=ffffff)](https://github.com/krishna310301)

</div>
