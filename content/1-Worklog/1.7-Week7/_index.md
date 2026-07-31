---
title: "Week 7 Worklog"
date: 2026-07-13
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# 7. ALB Load Balancing, CloudFront HTTPS & DNS Domain Setup

### Objectives of the week:

* Register SSL/TLS certificates on ACM and enforce HTTPS protocols.
* Set up Application Load Balancer (ALB) as a secure gateway for EC2 backend.
* Host frontend assets on S3, distribute via CloudFront CDN, and link custom domain.

### Tasks performed during the week:

| Day | Tasks performed | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| **Monday** | - Request a free public SSL/TLS certificate via ACM for `learnspherev2.id.vn`. | 07/13/2026 | 07/13/2026 | https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html |
| **Tuesday** | - Create an ALB in the public subnet, routing HTTPS requests on port 443 to the EC2 backend target group. | 07/14/2026 | 07/14/2026 | https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html |
| **Wednesday** | - Receive frontend build from Son, synchronize to S3, and create a CloudFront CDN distribution. | 07/15/2026 | 07/16/2026 | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html |
| **Thursday** | - Configure CNAME records in Tenten DNS panel pointing `www` to CloudFront and `api` to ALB. | 07/16/2026 | 07/17/2026 | https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html |
| **Friday** | - Fix Mixed Content issues by redirecting all frontend API endpoints to `api.learnspherev2.id.vn` subdomain. | 07/17/2026 | 07/17/2026 | https://aws.amazon.com/security/ |

### Key achievements of week 7:

* Successfully enforced HTTPS security protocols across the entire LearnSphere platform.
* Configured secure traffic routing from ALB in public subnets to EC2 instances in private subnets.
* Completed custom domain bindings, ensuring correct visual rendering and error-free API calls.
