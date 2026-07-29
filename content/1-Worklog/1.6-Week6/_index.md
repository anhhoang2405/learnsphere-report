---
title: "Week 6 Worklog"
date: 2026-07-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# Week 6 - Scaffolding Production Builds & Collaborating on AWS Infrastructure

### Week Objectives:

* Compile production builds for React Frontend and assist in containerizing Backend Express code.
* Collaborate on provisioning AWS resources (S3, ECR, EC2, IAM Role) securely.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Testing static compilation of React Frontend using Vite bundler. | 20/07/2026 | 20/07/2026 |
| 2 | Designing the `.dockerignore` file and assisting Nguyen Hong Son in reducing Docker container sizes. | 21/07/2026 | 21/07/2026 |
| 3 | Creating the AWS S3 Bucket (`learnsphere-fe-static`) to host static Frontend files. | 22/07/2026 | 22/07/2026 |
| 4 | Configuring EC2 Security Group ingress rules (restricting public port 5000 access). | 23/07/2026 | 23/07/2026 |
| 5 | Designing the IAM policies for the EC2 Instance Profile (`learnsphere-ec2-role`). | 24/07/2026 | 24/07/2026 |

### Week Achievements:

* Minified Frontend assets folder to less than 5MB to optimize global load speeds.
* Successfully created S3 Frontend Bucket and secured EC2 Security Group parameters.
* Finalized the keyless IAM Instance Profile design to allow secure S3/Bedrock access.
