---
title: "Week 3 Worklog"
date: 2026-06-15
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# 3. Amazon S3 Storage, CloudFront CDN & Dockerization

### Objectives of the week:

* Learn and configure Amazon S3 object storage for application media assets.
* Integrate CloudFront CDN to distribute static assets securely over HTTPS.
* Familiarize with Docker and pack a basic application into a container.

### Tasks performed during the week:

| Day | Tasks performed | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| **Monday** | - Create Amazon S3 Buckets for Frontend assets and Media files, configuring Block Public Access rules. | 06/15/2026 | 06/15/2026 | https://000005.awsstudygroup.com/ |
| **Tuesday** | - Create a CloudFront Distribution pointing to the S3 bucket and configure OAC to restrict direct S3 access. | 06/16/2026 | 06/16/2026 | https://000094.awsstudygroup.com/ |
| **Thursday** | - Study Dockerfile instructions, write a build script, and run a local Node.js application inside a container. | 06/18/2026 | 06/18/2026 | https://000015.awsstudygroup.com/ |
| **Friday** | - Create an Amazon ECR repository, push Docker image to ECR, and configure EC2 IAM Role to pull image. | 06/19/2026 | 06/19/2026 | https://000017.awsstudygroup.com/ |

### Key achievements of week 3:

* Successfully configured CloudFront distribution to serve static files and block direct S3 access.
* Mastered the core workflow of writing Dockerfiles and packaging containers.
* Pushed the first backend Docker image build to ECR for centralized repository storage.
