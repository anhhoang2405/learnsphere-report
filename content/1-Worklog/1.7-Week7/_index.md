---
title: "Week 7 Worklog"
date: 2026-07-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# Week 7 - HTTPS ALB, CloudFront & CI/CD Deployment (Deadline 31/07)

### Week Objectives:

* Configure Application Load Balancer (ALB) and ACM SSL cert for Backend HTTPS.
* Deploy Frontend to S3/CloudFront with custom domain alias and HTTPS.
* Establish automated CI/CD pipeline via GitHub Actions and release the system.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Requesting ACM SSL certificates and configuring Application Load Balancer listeners. | 27/07/2026 | 27/07/2026 |
| 2 | Configuring CloudFront static web distribution and setting up DNS aliases on Tenten. | 28/07/2026 | 28/07/2026 |
| 3 | Writing deploy.yml pipeline, configuring GitHub Secrets, and testing CI/CD workflow. | 29/07/2026 | 29/07/2026 |
| 4 | Fixing Bedrock Converse params API conflict and implementing AI fallback retries. | 30/07/2026 | 30/07/2026 |
| 5 | Configuring rate limits, applying restricted IAM policies, and publishing the final report. | 31/07/2026 | 31/07/2026 |

### Week Achievements:

* Completed full end-to-end HTTPS mapping for frontend (www.learnsphere.id.vn) and backend (api.learnsphere.id.vn).
* Integrated automatic failover retry logic (Groq ⇄ Bedrock) and fixed Bedrock param validations.
* Switched GitHub Actions credentials to a custom Least Privilege IAM policy and verified rate limits.
* Completed all deployment deliverables and submitted report before the July 31st deadline.
