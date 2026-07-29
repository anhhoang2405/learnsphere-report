---
title: "Blog 1"
date: 2026-07-26
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Deploying Node.js Backend to EC2 with Docker & IAM Roles

#### 1. Introduction
When deploying full-stack web applications on cloud platforms like AWS, keeping our backend services secure and lightweight is always a top priority. In this blog, I will share my journey of containerizing the **LearnSphere** backend using Docker and deploying it on an Amazon EC2 instance using a secure, keyless IAM configuration.

![Docker EC2 Deployment](/images/3-BlogsPosted/blog1.png)

---

#### 2. Why Containerization?
During development, we often run into the classic "works on my machine" problem. Variations in Node.js versions, dependencies, and OS environments can lead to unexpected crashes when deploying to a remote virtual server. 

By containerizing the Express backend with Docker, we bundle the application with all its required dependencies into a single, immutable container image. This guarantees that the code runs identically in local testing and in AWS production.

---

#### 3. Writing an Optimized Dockerfile
For production environments, security and size are critical. We use a **multi-stage build** to keep our final image extremely small, and we execute the code as a **non-root user** to prevent host system exposure in case of security breaches.

```dockerfile
# Stage 1: Install production dependencies
FROM node:20-alpine AS base
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production

# Stage 2: Copy Source & Execute
COPY src/ ./src/

# Security practice: Run as restricted non-root user
RUN addgroup -g 1001 -S nodejs && \
    adduser -S nodejs -u 1001
USER nodejs

EXPOSE 5000
ENV NODE_ENV=production

CMD ["node", "src/server.js"]
```

---

#### 4. The Power of AWS IAM Roles for EC2
One of the most common security mistakes in cloud deployments is hardcoding AWS Access Keys (`AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`) inside the `.env` configuration file on the virtual server. If the server is ever compromised, or if the environment files are accidentally committed to Git, the entire AWS account is exposed.

**The Solution**: Instead of access keys, we attach an **IAM Instance Profile** (named `learnsphere-ec2-role`) directly to our EC2 instance. 
1. Create an IAM Role with trust relationship allowed for `ec2.amazonaws.com`.
2. Attach permissions for S3 (`AmazonS3FullAccess`) and Bedrock (`AmazonBedrockFullAccess`).
3. Attach this role to the running EC2 instance.
4. The AWS SDK running inside the container will automatically query the EC2 Instance Metadata Service (IMDS) for temporary security credentials. 

This completely eliminates the need to store keys inside the `.env` file on EC2!

---

#### 5. Conclusion
By combining **Docker** and **AWS IAM Roles**, we achieve a highly secure, clean, and portable deployment model. The application remains isolated from the host OS, and authentication to AWS cloud storage is managed transparently without any static secrets.

---

### Community Proof (Facebook Post)
Below is the screenshot of the published article shared in the AWS Study Group Facebook community:

![Facebook Post Proof](/images/3-BlogsPosted/fb_post1.png)