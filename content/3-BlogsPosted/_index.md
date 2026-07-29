---
title: "Blogs Posted"
date: 2026-07-26
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

# Technical Blogs Posted

In this section, we list and introduce the technical articles shared with the cloud community at the [AWS Study Group Facebook Group](https://www.facebook.com/groups/awsstudygroupfcj) during the internship. These articles focus on containerization, HTTPS security, and automated deployment pipelines:

---

### [Blog 1: Deploying Node.js Backend to EC2 with Docker & IAM Roles](3.1-blog1/)
This article shares how we containerize the Node.js/Express backend using a multi-stage, non-root user Dockerfile for production execution, and connect it securely to AWS resources using an EC2 IAM Instance Profile role rather than storing static keys in environment files.

### [Blog 2: Solving Mixed Content: E2E HTTPS with CloudFront and ALB](3.2-blog2/)
This article explains the troubleshooting process for browser Mixed Content errors. We describe how we set up full end-to-end HTTPS decryption and traffic forwarding using AWS ACM certificates, Application Load Balancers (ALB) for the backend, and CloudFront CDN for the frontend React app.

### [Blog 3: Automating CI/CD with GitHub Actions: From Commit to Production in 3 Minutes](3.3-blog3/)
This article introduces our automated release pipeline. We outline how we configure GitHub Actions to automatically run tests, build and sync frontend static files to S3, build and push backend Docker containers to ECR, deploy via EC2 SSH command sequences, and invalidate CloudFront CDN caches.