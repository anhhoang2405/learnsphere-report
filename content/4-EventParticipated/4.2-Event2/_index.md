---
title: "Event 2"
date: 2026-07-25
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: Attending Demo Day - ASEAN Agentic AI Buildathon (AABW)

### 1. General Event Information
*   **Event Name:** ASEAN Agentic AI Buildathon (AABW) - Demo Day & Project Showcase
*   **Date & Time:** 09:00 - 12:00, July 25, 2026
*   **Location:** AWS Vietnam Office Hall, Ho Chi Minh City
*   **Role:** Attendee

---

### 2. Event Objectives
*   Understand the latest trends and real-world applications of Agentic AI (AI Systems with autonomous agents) through projects developed by participating teams.
*   Analyze cloud solution architectures of large-scale systems, specifically studying how AWS services (Amazon Bedrock, SageMaker, Lambda) are integrated with advanced AI foundation models.
*   Gain insight into rapid prototyping workflows under strict time limits (24-hour hackathons) and observe professional pitching techniques in front of AWS expert judges.

---

### 3. Analysis of Outstanding Projects
During the Demo Day, I analyzed the architecture and cloud infrastructure of several innovative projects:

#### A. S.H.E.P.H.E.R.D (Team 3KA)
*   **Goal:** A smart system designed to monitor crowd density, analyze queue conditions, and predict real-time congestion during massive public events.
*   **Technical Architecture:** 
    *   Leveraged **YOLO + ByteTrack** for real-time person detection and motion tracking from camera feeds.
    *   Hosted AI inference engines on **Amazon SageMaker Endpoints** to process video analysis.
    *   Integrated **Amazon Bedrock AgentCore + Strands Agent** to orchestrate actions and trigger proactive alerts onto a React monitoring dashboard.

#### B. Signal Scout (Team Signal Scout)
*   **Goal:** An autonomous AI Agent that automatically crawls and analyzes market signals to alert corporate strategy teams of potential risks early.
*   **Technical Architecture:** 
    *   Used **Apify & TinyFish** to crawl data sources from various public web channels.
    *   Automated data ingestion workflows using **Amazon API Gateway -> AWS Lambda** to persist raw signals into **Amazon DynamoDB**.
    *   Utilized **AgentCore Runtime** coupled with **Amazon Bedrock** and **Bedrock Guardrails** to process private data securely and guarantee safe text output.

#### C. KFC Bot Agent (Team One Team)
*   **Goal:** A conversational multi-channel AI ordering assistant (integrated with Zalo OA, Messenger, and WhatsApp) that eliminates friction by skipping app downloads or registration flows.
*   **Technical Architecture:** 
    *   User messages received via Zalo are handled by **AWS WAF & API Gateway**, then pushed into **Amazon SQS** queues to balance compute loads.
    *   Managed dialog logic and order validation using **Bedrock AgentCore** paired with **Amazon OpenSearch Service** for vector search.
    *   Reduced infrastructure code by **60%** by relying heavily on AWS's built-in AgentCore framework.

---

### 4. Key Takeaways & Lessons Learned
*   **A Deeper Appreciation of Agentic AI:** Learned the fundamental differences between basic conversational chatbots (single response models) and actual AI Agents (which possess planning skills, tool calling capabilities, autonomous decision loops, and short/long-term memory).
*   **Serverless Architectural Design:** Observed how teams optimized cloud hosting costs (e.g., Team Signal Scout reducing their monthly AWS cost estimate from $130 to $35 by implementing cost-efficient Lambda and Bedrock invocation models).
*   **Motivation for Personal Growth:** Observed the dedication of teams debugging code at 3:00 AM, dealing with sleep deprivation, and producing functioning MVPs. This serves as great inspiration for my own final work on the LearnSphere platform.

---

### 5. Event Verification Photos
Below is the photo capturing the dynamic presentations and technology showcases during the Demo Day:

![AABW Demo Day Proof 1](/images/4-EventParticipated/event2a.jpg)
![AABW Demo Day Proof 2](/images/4-EventParticipated/event2b.jpg)
