---
title: "Week 6 Worklog"
date: 2026-07-06
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# 6. Backend Containerization & EC2 Deployment

### Objectives of the week:

* Optimize Dockerfile with multi-stage builds for security and smaller footprint.
* Install and set up the production environment for Express backend on EC2.
* Write bash scripts to automate container pull and restart processes.

### Tasks performed during the week:

| Day | Tasks performed | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| **Monday** | - Write a multi-stage Dockerfile using lightweight alpine base images running under non-root users. | 07/06/2026 | 07/06/2026 | https://docs.docker.com/develop/develop-images/multistage-build/ |
| **Tuesday** | - Launch a production EC2 instance (`t3.small`) in the private subnet of the VPC. | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html |
| **Thursday** | - Install Docker on EC2 and configure 2GB of Swap space to prevent out-of-memory issues. | 07/09/2026 | 07/09/2026 | https://docs.docker.com/engine/install/ |
| **Friday** | - Pull the backend image from ECR to EC2 and write a shell script to automate pulling new images and restarting. | 07/10/2026 | 07/10/2026 | https://docs.aws.amazon.com/AmazonECR/latest/userguide/image-pull-ecr.html |

### Key achievements of week 6:

* Optimized Dockerfile reducing image size from 900MB to 150MB.
* Configured Swap space successfully on EC2 to ensure database and application stability under load.
* Backend container successfully runs on EC2 and connects securely to MongoDB Atlas.
