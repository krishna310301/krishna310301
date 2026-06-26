<div align="center">

# Krishna Koushik Thokala

### Cloud Infrastructure Engineer | AWS, EKS, Terraform, GitOps, CloudWatch

Production infrastructure operations shaped how I build cloud systems: observable, automated, secure, and built for recovery.

<p>
  <a href="https://linkedin.com/in/krishna3103">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="mailto:krishnakoushikthokala@gmail.com">krishnakoushikthokala@gmail.com</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/krishna310301">GitHub</a>
  &nbsp;·&nbsp;
  Austin, TX
</p>

Open to Cloud Infrastructure Engineer, Cloud Engineer, Platform Engineer, Infrastructure Engineer, Associate SRE, and DevOps Engineer roles.

</div>

---

## Why I Build Cloud Systems This Way

Before moving deeper into cloud engineering, I spent 2+ years in production infrastructure operations at Tata Communications. I supported SLA-driven incident response, RCA, TAC/vendor coordination, field dispatch, operational handoffs, and 24/7 troubleshooting across carrier-grade networks.

That background matters because I have seen infrastructure fail in production. I have worked through BGP/MPLS routing failures, TCP/IP connectivity issues, DWDM optical transport faults, submarine cable handoffs, and multi-vendor escalations where clear ownership and clean handoffs mattered.

Now I build cloud infrastructure projects with that same operations-first mindset. I care about how systems are deployed, monitored, scaled, secured, debugged, and recovered when something breaks.

```yaml
current_focus:
  - AWS cloud infrastructure
  - Kubernetes and Amazon EKS
  - GitOps delivery with Argo CD
  - Terraform infrastructure as code
  - Dockerized services and CI/CD
  - CloudWatch observability and incident workflows
  - Platform engineering foundations

background:
  - 2+ years production network operations
  - SLA-driven incident response and RCA
  - 25-30 Tier-1 carrier clients across global ILL, DWDM, and submarine cable networks
  - BGP, MPLS, TCP/IP, DWDM, and segment-wise fault isolation
  - MS Computer Science, Indiana University Bloomington
  - AWS Certified Cloud Practitioner
```

---

## Featured Platform Projects

### [CloudOps SRE Platform](https://github.com/krishna310301/cloudops-sre-platform)

CloudOps SRE Platform is where I moved my operations background into AWS. It runs a React/FastAPI reliability dashboard on EKS and tracks the things I wanted during live incidents: service health, deployment history, incident timelines, MTTR, SLOs, and error budget views.

![CloudOps SRE Platform Architecture](https://raw.githubusercontent.com/krishna310301/cloudops-sre-platform/main/docs/architecture/cloudops-sre-platform-architecture.png)

**What I focused on**

- React and FastAPI workloads deployed behind ALB Ingress on Amazon EKS
- Helm-managed Kubernetes deployments, services, resource limits, readiness/liveness probes, and Secrets Manager-backed database credentials
- Terraform-managed AWS infrastructure across VPC, EKS, ECR, RDS PostgreSQL, IAM, Secrets Manager, security groups, and CloudWatch
- SRE workflows for service catalog, deployment history, P1-P4 incidents, incident timelines, MTTR, SLO tracking, and error budget views
- HPA validation under k6 load where backend replicas scaled from 2 to 6 pods, sustaining 2,035 requests at a 99.5% success rate with 1.52s p95 latency
- Short-lived AWS run with EKS resources, CloudWatch logs, HPA screenshots, and same-day Terraform destroy for cost control

**Tech:** AWS, EKS, Kubernetes, Helm, Terraform, Docker, ECR, RDS PostgreSQL, ALB Ingress, CloudWatch, GitHub Actions, FastAPI, React

**Links:** [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Run screenshots](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/screenshots/aws-demo-2026-06-06) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture/cloudops-sre-platform-architecture.png)

---

### [CloudOps GitOps Platform](https://github.com/krishna310301/cloudops-gitops-platform)

CloudOps GitOps Platform builds on the SRE platform. After deploying workloads to EKS, I built the delivery path around Kubernetes: Git-managed environments, Argo CD reconciliation, promotion through pull requests, drift correction, and rollback through Git.

**What I focused on**

- Argo CD AppProject and multi-source Applications for `dev`, `staging`, and `prod`
- Helm values kept outside the chart through the documented `$values/...` pattern
- Terraform-provisioned VPC, EKS, ECR, IAM, security groups, and public subnets
- Namespace-scoped ResourceQuotas, Roles, RoleBindings, and ServiceAccounts
- GitHub Actions workflow for app tests, Helm rendering, Argo CD manifest rendering, image build, and optional ECR push
- PR-style image promotion through Git-managed Helm values
- Drift self-healing after manual replica changes and Git revert rollback after a Helm-toggled readiness failure
- Local kind validation, EKS validation, screenshot output, and Terraform destroy after the AWS run

**Tech:** AWS, EKS, Argo CD, Kubernetes, Helm, Terraform, ECR, GitHub Actions, Docker, Python

**Links:** [Repository](https://github.com/krishna310301/cloudops-gitops-platform) · [Validation output](https://github.com/krishna310301/cloudops-gitops-platform/tree/main/docs/screenshots) · [Architecture](https://github.com/krishna310301/cloudops-gitops-platform/blob/main/docs/architecture.md)

---

## Serverless Monitoring Project

### [CloudOps Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor)

CloudOps Uptime Monitor shows the same operations mindset outside Kubernetes. It checks website availability every 5 minutes, stores current and historical status in DynamoDB, sends state-change alerts, and serves a React dashboard through CloudFront.

- Built on EventBridge, Lambda, DynamoDB, API Gateway, SNS, CloudWatch, Terraform, and React on S3/CloudFront
- Optimized current-status reads from 86,400 history records to 10 latest-status rows for a 10-URL, 30-day workload
- Added API keys, throttling, restricted CORS, KMS, DLQs, state-change alerts, 9 CloudWatch metrics, and CI quality gates
- Hardened URL intake with unsafe target blocking and redirect validation to avoid monitoring risky internal or reserved addresses

**Tech:** Lambda, DynamoDB, API Gateway, EventBridge, SNS, S3, CloudFront, CloudWatch, Terraform, React, GitHub Actions

---

## Technical Focus

| Area | Tools and Concepts |
|---|---|
| Cloud | AWS, VPC, IAM, EC2, S3, Lambda, API Gateway, EventBridge, CloudWatch, SNS, DynamoDB, CloudFront, EKS, ECR, RDS, ALB, Secrets Manager |
| Infrastructure and DevOps | Terraform, Docker, Kubernetes, Amazon EKS, Helm, Argo CD, GitOps, GitHub Actions, Git, CI/CD, Linux, Ingress, ConfigMaps, Secrets, readiness/liveness probes, HPA, k6 |
| Observability and SRE | CloudWatch logs, metrics, alarms, HPA, incident response, RCA, runbooks, SLA-driven troubleshooting, MTTR, SLO-style metrics |
| Networking | TCP/IP, BGP, OSPF, MPLS, VPN, DNS, load balancing, firewalls, Juniper/Cisco routing |
| Programming | Python, Bash, SQL, PostgreSQL, REST APIs, FastAPI, React |

---

## Experience

### Tata Communications, Senior Engineer, Shift Lead - Production NOC Operations

Owned high-severity production infrastructure incidents across 25-30 Tier-1 carrier clients on global ILL, DWDM, and submarine cable networks.

- Drove triage, TAC/vendor coordination, field dispatch, submarine handoffs, and service restoration across 24/7 NOC operations
- Isolated BGP/MPLS failures, TCP/IP issues, DWDM faults, and equipment malfunctions across Juniper, Huawei, Ciena, and Alcatel platforms
- Led 5-person global NOC shifts through 40+ daily priority incidents, including AVP/VP-level escalations, RCA notes, customer-premises testing, and cross-functional follow-up
- Restored high-priority services within 4-hour SLA targets and contributed to 99.9% annual network availability; earned Certificate of Excellence

---

## Education and Certifications

- MS Computer Science, Indiana University Bloomington, May 2026
- B.Tech Computer Science and Engineering, SRM Institute of Science and Technology
- AWS Certified Cloud Practitioner, 2026

---

## GitHub Activity

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=krishna310301&theme=tokyonight&hide_border=true&background=0d1117&ring=38BDF8&fire=0EA5E9&currStreakLabel=38BDF8&sideLabels=CBD5E1&dates=94A3B8)](https://github.com/krishna310301)

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=krishna310301&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=38BDF8&line=0EA5E9&point=ffffff)](https://github.com/krishna310301)

![Profile Views](https://komarev.com/ghpvc/?username=krishna310301&color=0EA5E9&style=flat-square&label=profile+views)

</div>

---

<div align="center">

Infrastructure is invisible when it works, and everything when it does not.

</div>
