---
title: "Week 6 Worklog"
date: 2026-07-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# 6. Docker Containerization, ECR & EC2 Server Setup

### Week Objectives:

* Containerize the Backend codebase using multi-stage Docker builds to optimize size and enhance security.
* Create AWS ECR repositories, launch EC2 host servers, configure Swap space virtual memory, and associate IAM Instance Profile roles.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Wrote a multi-stage Dockerfile utilizing a `node:24-alpine` base image, configuring the container runtime to run under a secure non-root user. | 20/07/2026 | 20/07/2026 |
| 2 | Initialized the Amazon ECR repository to store and version control backend Docker images. | 21/07/2026 | 21/07/2026 |
| 3 | Launched an EC2 `t3.small` instance on AWS, installed Docker, and allocated 2GB of Swap virtual memory to prevent RAM exhaustion. | 22/07/2026 | 22/07/2026 |
| 4 | Customized EC2 Security Group rules, closing public port 22 SSH ingress and restricting traffic exclusively to secure web pathways. | 23/07/2026 | 23/07/2026 |
| 5 | Created and attached the IAM Instance Profile role (`learnsphere-ec2-role`) allowing EC2 to pull ECR images and push system logs to CloudWatch. | 24/07/2026 | 24/07/2026 |

### Week Achievements:

* Successfully dockerized the backend service, creating secure, lightweight production container profiles.
* Successfully provisioned the EC2 target hosting host with Swap memory safety buffers and secured it with IAM instance profiles.
