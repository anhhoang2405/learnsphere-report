---
title: "Week 7 Worklog"
date: 2026-07-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# 7. HTTPS ALB, CloudFront CDN & CI/CD Automation

### Week Objectives:

* Configure CloudFront CDN for Frontend and set up Application Load Balancer (ALB) routing for EC2 Backend under secure HTTPS.
* Establish automated CI/CD pipelines via GitHub Actions (OIDC) and run live production verification.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Received the static Frontend build from Son, uploaded it to S3, and configured CloudFront CDN with OAC for secure S3 access. | 27/07/2026 | 27/07/2026 |
| 2 | Registered SSL certificates on ACM for `learnspherev2.id.vn`, set up ALB listening on port 443, and forwarded traffic to EC2 port 5000. | 28/07/2026 | 28/07/2026 |
| 3 | Configured CNAME records on Tenten: pointed `www` to CloudFront CDN, and `api` to ALB to completely resolve Mixed Content issues. | 29/07/2026 | 29/07/2026 |
| 4 | Developed and finalized the GitHub Actions workflow file (`deploy.yml`), setting up OIDC for keyless secure AWS authentication. | 30/07/2026 | 30/07/2026 |
| 5 | Ran the CI/CD pipeline automation tests (push to main triggers auto-deployment); conducted E2E testing with Son and Dung, and submitted the report. | 31/07/2026 | 31/07/2026 |

### Week Achievements:

* Successfully deployed the LearnSphere system live with full end-to-end HTTPS encryption under the domain `https://www.learnspherev2.id.vn`.
* Established automated deployment pipelines for Backend on EC2 and Frontend on S3, completing builds in under 3 minutes.
* Concluded the internship and submitted the final sign-off report before the July 31st deadline.
