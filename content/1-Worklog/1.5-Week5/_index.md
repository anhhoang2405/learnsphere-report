---
title: "Week 5 Worklog"
date: 2026-07-25
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# 5. AI Service Integration & Local Integration Testing

### Week Objectives:

* Request model access on AWS Bedrock and integrate the Bedrock Converse API and Groq API into the Backend.
* Conduct comprehensive local End-to-End full-stack testing and resolve CORS connection errors.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Accessed AWS Console to submit a Model Access request for Anthropic Claude models on Amazon Bedrock. | 13/07/2026 | 13/07/2026 |
| 2 | Wrote the `ai-provider.service.js` backend service wrapper acting as a unified portal for AWS Bedrock SDK and Groq API. | 14/07/2026 | 14/07/2026 |
| 3 | Developed the Backend router and controllers for the AI Chatbot (`/api/ai/chat`) and automated quiz generation. | 15/07/2026 | 15/07/2026 |
| 4 | Supported Son in connecting the React Frontend with Backend AI endpoints, configuring Express CORS middleware to handle preflights. | 16/07/2026 | 16/07/2026 |
| 5 | Ran local E2E workflow tests: Login -> Create Course -> S3 Upload -> AI Quiz Generation -> AI Tutor Chat session. | 17/07/2026 | 17/07/2026 |

### Week Achievements:

* Successfully integrated AI engines (AWS Bedrock Claude & Groq), achieving fast response times under 2 seconds.
* Resolved CORS preflight errors when the React client sends authorization tokens in custom request headers.
* The entire LearnSphere application runs smoothly locally and is ready for AWS cloud staging.
