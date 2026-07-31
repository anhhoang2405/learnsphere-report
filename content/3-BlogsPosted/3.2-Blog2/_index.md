---
title: "Blog 2"
date: 2026-07-26
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Solving Mixed Content: E2E HTTPS with CloudFront and ALB

#### 1. Introduction
When launching a full-stack project in production, the most frustrating moment is when everything works on HTTP, but the moment you enable SSL, login buttons stop working and return cryptic `Failed to fetch` network errors. In this article, I will explain why this happens (the **Mixed Content** issue) and how to resolve it using AWS CloudFront, Application Load Balancers, and ACM SSL certificates.

![HTTPS SSL Configuration](/images/3-BlogsPosted/blog2.png)

---

#### 2. What is "Mixed Content"?
Modern web browsers enforce strict security rules. If your main website is served over a secure, encrypted connection (**HTTPS**), the browser blocks all requests from that page to unencrypted resources (**HTTP**).

In our early deployment, we served the React frontend securely via HTTPS using CloudFront. However, the backend container on EC2 was exposed using a raw IP and HTTP protocol (`http://18.143.151.54:5000`).
When a user entered their credentials on `https://www.learnspherev2.id.vn` and clicked Login, the browser blocked the API call to `http://18.143.151.54:5000/api/auth/login` to prevent data sniffing, triggering a fatal `TypeError: Failed to fetch` console error.

---

#### 3. Resolving the Issue with AWS Application Load Balancer
To fix Mixed Content, both frontend and backend must run on HTTPS. Since raw IP addresses cannot hold SSL certificates, we must use a custom domain name and route traffic through a load balancer.

We set up an **Application Load Balancer (ALB)** to act as the HTTPS gatekeeper:
```
User (Browser) ───► HTTPS:443 ──► AWS ALB (SSL Decryption) ──► HTTP:5000 ──► EC2 Backend
```
1. **Request Certificate**: Issue free SSL certificates using AWS Certificate Manager (ACM) for our custom domain: `learnspherev2.id.vn` and `*.learnspherev2.id.vn`.
2. **Configure ALB Listener**: Set up the ALB to listen on HTTPS port 443, attach the ACM certificate, and target port 5000 of our EC2 instance.
3. **Register DNS CNAME**: Point `api.learnspherev2.id.vn` in our domain settings to the Load Balancer DNS.

Now, all API endpoints are securely accessible at `https://api.learnspherev2.id.vn/api/`!

---

#### 4. Frontend SSL & CloudFront Configuration
For the frontend, we use Amazon CloudFront to serve the static build files from S3:
1. Issue another ACM SSL certificate for `www.learnspherev2.id.vn` in the **US East (N. Virginia - `us-east-1`)** region (a global requirement for CloudFront).
2. Attach the domain alias and the N. Virginia certificate to the CloudFront distribution.
3. Turn on the **Redirect HTTP to HTTPS** viewer policy to force secure connections for all visitors.
4. Set a custom CNAME on our registrar pointing `www` to the CloudFront distribution domain.

---

#### 5. Conclusion
With both Frontend (`https://www.learnspherev2.id.vn`) and Backend API (`https://api.learnspherev2.id.vn`) fully encrypted on HTTPS, the Mixed Content security blocker is satisfied. Data transmitted between the user's browser and AWS is encrypted end-to-end, making our system secure and professional.

---

### Community Proof (Facebook Post)
Below is the screenshot of the published article shared in the AWS Study Group Facebook community:

![Facebook Post Proof](/images/3-BlogsPosted/fb_post2.png)