---
title: "Week 7 Worklog"
date: 2026-07-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# Week 7 - Frontend S3/CloudFront Deployment & System Sign-off (Deadline 31/07)

### Week Objectives:

* Deploy React Frontend static client to S3 Web Hosting and secure access using HTTPS CloudFront CDN.
* Configure custom domain alias mapping and collaborate on verifying GitHub Actions CI/CD workflows.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Syncing minified Frontend production assets to the target `learnsphere-fe-static` S3 bucket. | 27/07/2026 | 27/07/2026 |
| 2 | Provisioning CloudFront CDN, setting up Custom Error Page routing (404 redirects to `/index.html`). | 28/07/2026 | 28/07/2026 |
| 3 | Configuring CNAME record alias `www` pointing to CloudFront host domain on Tenten.vn. | 29/07/2026 | 29/07/2026 |
| 4 | Collaborating with Nguyen Hong Son to verify GitHub Secrets and test automated deploy actions. | 30/07/2026 | 30/07/2026 |
| 5 | Carrying out final validation tests over live HTTPS endpoints and submitting the internship report. | 31/07/2026 | 31/07/2026 |

### Week Achievements:

* Successfully deployed web client on custom secure domain: **`https://www.learnsphere.id.vn`**.
* CI/CD automation working flawlessly (auto-syncing assets to S3 and invalidating CloudFront distribution paths `/*` on pushes).
* Submitting report ahead of the final July 31st deadline.
