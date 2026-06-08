<div align="center">

# Krishna Koushik Thokala

### Cloud Engineer | AWS, EKS/Kubernetes, Terraform, Docker, CloudWatch

Production network operations shaped how I build cloud systems: observable, automated, secure, and reliable by default.

<p>
  <a href="https://linkedin.com/in/krishna3103">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="mailto:krishnakoushikthokala@gmail.com">krishnakoushikthokala@gmail.com</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/krishna310301">GitHub</a>
  &nbsp;·&nbsp;
  Austin, TX · Open to U.S. cloud/SRE roles
</p>

Open to Cloud Engineer, Cloud Infrastructure Engineer, Junior DevOps Engineer, Associate SRE, and Cloud Operations Engineer roles.

</div>

---

## Why I Build Cloud Systems This Way

Before moving deeper into cloud engineering, I spent 2+ years in production network operations at Tata Communications. I supported SLA-driven incident response, RCA, vendor coordination, runbooks, operational handoffs, and 24/7 troubleshooting across carrier-grade infrastructure.

That background matters because I have seen infrastructure fail in production. I have worked through BGP/MPLS routing failures, TCP/IP connectivity issues, DWDM optical transport faults, 100G circuit incidents, and multi-vendor escalations where clear ownership and clean handoffs mattered.

Now I build cloud projects with that same operations-first mindset. I care about how systems are deployed, monitored, scaled, secured, debugged, and recovered when something breaks.

```yaml
current_focus:
  - AWS cloud infrastructure
  - Kubernetes and Amazon EKS
  - Terraform infrastructure as code
  - Dockerized services and CI/CD
  - CloudWatch observability and incident workflows

background:
  - 2+ years production network operations
  - SLA-driven incident response and RCA
  - BGP, MPLS, TCP/IP, DWDM, 100G carrier circuits
  - MS Computer Science, Indiana University Bloomington
  - AWS Certified Cloud Practitioner
```

---

## Featured Project

### [CloudOps SRE Platform](https://github.com/krishna310301/cloudops-sre-platform)

CloudOps SRE Platform is a cloud-native reliability operations dashboard built on Amazon EKS. It tracks service health, deployments, incidents, incident timelines, MTTR, and SLO-style reliability metrics.

![CloudOps SRE Platform Architecture](https://raw.githubusercontent.com/krishna310301/cloudops-sre-platform/main/docs/architecture/cloudops-sre-platform-architecture.png)

**What I focused on**

- Amazon EKS deployment with Kubernetes Deployments, Services, ALB Ingress, Helm, resource limits, readiness/liveness probes, and HPA autoscaling
- AWS infrastructure with Terraform: VPC, EKS, ECR, RDS PostgreSQL, IAM, Secrets Manager, security groups, and CloudWatch
- Production-style app stack with React, FastAPI, PostgreSQL/RDS, Docker, ECR, and GitHub Actions
- SRE product workflows: service catalog, deployment history, P1-P4 incidents, incident timelines, MTTR, health dashboard, and reliability status
- Short-lived AWS demo run with screenshots, HPA load testing, CloudWatch logs, EKS resources, and same-day Terraform destroy for cost control

**Tech:** AWS, EKS, Kubernetes, Helm, Terraform, Docker, ECR, RDS PostgreSQL, ALB Ingress, CloudWatch, GitHub Actions, FastAPI, React

**Links:** [Repository](https://github.com/krishna310301/cloudops-sre-platform) · [Demo screenshots](https://github.com/krishna310301/cloudops-sre-platform/tree/main/docs/screenshots/aws-demo-2026-06-06) · [Architecture](https://github.com/krishna310301/cloudops-sre-platform/blob/main/docs/architecture/cloudops-sre-platform-architecture.png)

---

## Currently Improving

I am still using CloudOps SRE Platform as a place to practice production hardening. Current roadmap items are tracked in the repo's [open issues](https://github.com/krishna310301/cloudops-sre-platform/issues).

- SLO/error budget tracking for service reliability views
- Structured JSON logging and request correlation IDs
- Release tagging and image promotion workflow
- Kubernetes manifest validation in CI
- RDS connectivity and secret rotation runbook
- Optional Grafana/kube-prometheus-stack observability pass

---

## Other Cloud Projects

### [CloudOps Uptime Monitor](https://github.com/krishna310301/cloudops-uptime-monitor)

Serverless AWS uptime monitoring application with a live React dashboard.

- EventBridge triggers Lambda every 5 minutes to check service availability
- DynamoDB stores status codes, latency, and uptime history
- SNS sends downtime alerts
- S3 and CloudFront host the frontend dashboard
- Terraform provisions AWS infrastructure and GitHub Actions automates deployment

**Tech:** Lambda, DynamoDB, API Gateway, EventBridge, SNS, S3, CloudFront, CloudWatch, Terraform, React, GitHub Actions

### [AWS Incident Triage Pipeline](https://github.com/krishna310301/aws-incident-triage-pipeline)

Event-driven AWS incident response workflow that turns CloudWatch alarms into structured triage summaries.

- CloudWatch alarms trigger Lambda through SNS
- Lambda parses alert context and calls Amazon Bedrock
- Bedrock assists with likely causes, severity, and remediation guidance
- Terraform provisions Lambda, SNS, IAM, CloudWatch alarms, and Bedrock access

**Tech:** AWS Lambda, CloudWatch, SNS, Amazon Bedrock, Terraform, IAM, Python, GitHub Actions

---

## Technical Focus

| Area | Tools and Concepts |
|---|---|
| Cloud | AWS, EC2, S3, VPC, IAM, Lambda, API Gateway, EventBridge, CloudWatch, SNS, DynamoDB, CloudFront, EKS, ECR, RDS, ALB |
| Kubernetes and DevOps | Kubernetes, Amazon EKS, Helm, Docker, Terraform, GitHub Actions, CI/CD, Linux, Bash, Git |
| Observability and Operations | CloudWatch Logs, metrics, alarms, HPA, incident response, RCA, runbooks, SLA-driven troubleshooting |
| Networking | TCP/IP, BGP, OSPF, MPLS, VPN, DNS, load balancing, firewalls, Juniper/Cisco routing |
| Programming | Python, Bash, SQL, PostgreSQL, REST APIs, FastAPI, React |

---

## Experience

### Tata Communications, Senior Network Engineer, Shift Lead

Supported high-availability carrier infrastructure for global telecom and enterprise clients across Juniper, Huawei, Ciena, and Alcatel environments.

- Troubleshot BGP/MPLS routing failures, TCP/IP connectivity issues, DWDM optical transport faults, and 100G carrier circuit incidents
- Led a 5-person global NOC shift handling 40+ daily P1/P2 incidents across 24/7 operations
- Coordinated triage, escalation, vendor communication, RCA documentation, and operational handoffs
- Achieved 4-hour SLA compliance for high-priority incidents and earned a Certificate of Excellence for operational reliability

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
