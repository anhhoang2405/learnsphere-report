---
title: "Week 9 Worklog"
date: 2026-07-27
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# 9. CI/CD Pipeline Automation & Internship Handover

### Objectives of the week:

* Build a fully automated CI/CD pipeline for backend and frontend deployment.
* Securely manage application environmental secrets using AWS Systems Manager.
* Finalize the internship report and present the project.

### Tasks performed during the week:

| Day | Tasks performed | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| **Monday** | - Set up GitHub Actions CI/CD workflow utilizing AWS OIDC authentication for secure deployments. | 07/27/2026 | 07/28/2026 | https://docs.github.com/en/actions |
| **Tuesday** | - Develop pipeline scripts to build, tag, push backend images to ECR, and deploy on EC2. | 07/28/2026 | 07/29/2026 | https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services |
| **Wednesday** | - Store application configurations (`MONGO_URI`, `JWT_SECRET`, etc.) securely in SSM Parameter Store. | 07/29/2026 | 07/29/2026 | https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html |
| **Thursday** | - Execute end-to-end (E2E) testing of the CI/CD pipeline, checking deployment success on commit pushes. | 07/30/2026 | 07/30/2026 | https://docs.github.com/en/actions/automating-builds-and-tests/about-continuous-integration |
| **Friday** | - Document all configuration settings, take screenshots of AWS consoles, and submit the report. | 07/31/2026 | 07/31/2026 | https://aws.amazon.com/blogs/devops/ |

### Key achievements of week 9:

* Active and robust CI/CD pipelines deploying updates to S3 and EC2 in under 3 minutes.
* Secured all database credentials and API keys using SSM Parameter Store and OIDC role assumptions.
* Successfully completed the internship and handed over the LearnSphere platform to the advisors.
