---
title: "Blog 3"
date: 2026-07-26
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Automating CI/CD with GitHub Actions: From Commit to Production in 3 Minutes

#### 1. Introduction
In a modern development team, speed and reliability are crucial. Running build scripts locally, manually dragging files to S3, and SSH-ing into EC2 to pull Docker images every time you make a small UI edit is highly inefficient. In this blog, I will share how we built an automated **CI/CD pipeline using GitHub Actions** for the **LearnSphere** platform.

![CI/CD Pipeline](/images/3-BlogsPosted/blog3.png)

---

#### 2. The Architecture of Our Pipeline
We use a **decoupled workflow** triggered automatically whenever a push commit is merged into the `main` branch of our GitHub repository. The runner splits the work into two parallel jobs:

1. **Backend Deployment**:
   - Compiles and checks Node.js source files.
   - Automatically logs into AWS ECR.
   - Builds a fresh Docker container image using the `latest` and `SHA` tags.
   - Pushes the image to ECR.
   - Connects to our EC2 host via SSH, pulls the new image, stops the old container, and starts the new one.
2. **Frontend Deployment**:
   - Installs node dependencies and executes the Vite build compiler.
   - Connects to AWS S3 and syncs compiled `/dist` static files.
   - Invalidate the CloudFront CDN cache paths (`/*`) so users get the fresh React updates immediately.

---

#### 3. Security Best Practice: Least Privilege Policies
A major risk with automated CI/CD runners is permission management. Giving the GitHub runner full administrator access (`AdministratorAccess`) to your AWS account is extremely dangerous. If your GitHub repository is compromised, attackers gain full access to your cloud assets.

To prevent this, we design a custom **Least Privilege IAM Policy** for the GitHub Actions user:
* Enforce write permission restricted **only** to the static frontend S3 bucket.
* Restrict ECR push rights **only** to the specific backend repository `learnsphere-be`.
* Restrict cache invalidation rights **only** to the specific CloudFront distribution ID.

This limits the blast radius and secures the cloud account.

---

#### 4. The Deployment Script (`deploy.yml`)
The workflow is defined under `.github/workflows/deploy.yml`. It consumes secure **GitHub Secrets** variables (like `AWS_ACCESS_KEY_ID`, `EC2_HOST`, and `EC2_SSH_KEY`) injected dynamically during execution. The runner leverages standard AWS action templates (`aws-actions/configure-aws-credentials`, `aws-actions/amazon-ecr-login`) to handle secure connections transparently.

---

#### 5. Conclusion
With this CI/CD pipeline in place, our team has achieved **zero-downtime automated deployments**. Developers no longer need access to AWS consoles or server SSH keys to update the system. They simply focus on writing high-quality code, pushing to Git, and watching their changes go live globally in under 3 minutes!

---

### Community Proof (Facebook Post)
Below is the screenshot of the published article shared in the AWS Study Group Facebook community:

![Facebook Post Proof](/images/3-BlogsPosted/fb_post3.png)