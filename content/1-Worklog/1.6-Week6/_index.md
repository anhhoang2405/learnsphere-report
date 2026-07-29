---
title: "Week 6 Worklog"
date: 2026-07-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# Week 6 - Docker Containerization & Server Setup

### Week Objectives:

* Dockerize the Backend application using a multi-stage non-root user design.
* Launch target EC2 instance, configure S3 buckets, and ECR repositories.
* Attach IAM roles for keyless AWS authentication.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Writing optimized production multi-stage backend Dockerfile. | 20/07/2026 | 20/07/2026 |
| 2 | Adding non-root user and verifying container builds locally. | 21/07/2026 | 21/07/2026 |
| 3 | Creating S3 buckets for static hosting and ECR repositories. | 22/07/2026 | 22/07/2026 |
| 4 | Launching EC2 instance and installing Docker daemon. | 23/07/2026 | 23/07/2026 |
| 5 | Configuring EC2 IAM instance profiles and running backend container manually. | 24/07/2026 | 24/07/2026 |

### Week Achievements:

* Authored a production-ready, non-root user Backend Dockerfile.
* Launched Amazon Linux 2023 EC2 instance and installed Docker daemon.
* Attached IAM Instance Profile `learnsphere-ec2-role` to EC2 for keyless S3/Bedrock access.
