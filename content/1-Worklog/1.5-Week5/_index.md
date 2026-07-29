---
title: "Week 5 Worklog"
date: 2026-07-25
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# Week 5 - AI Core Service Integration & Local Testing

### Week Objectives:

* Integrate AI helper features (Chatbot, summarization, quiz parser).
* Write flexible provider layers to call Groq (Llama-3) and Bedrock APIs.
* Verify the application full-stack locally and resolve CORS/JWT issues.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Researching Groq and AWS Bedrock Converse API request schemas. | 13/07/2026 | 13/07/2026 |
| 2 | Implementing chat endpoints, lesson summarizer, and quiz generator parser. | 14/07/2026 | 14/07/2026 |
| 3 | Configuring Groq API integration and Bedrock fallback structure. | 15/07/2026 | 15/07/2026 |
| 4 | Debugging backend CORS policies and authentication middlewares. | 16/07/2026 | 16/07/2026 |
| 5 | Testing end-to-end local platform flow using mock data. | 17/07/2026 | 17/07/2026 |

### Week Achievements:

* Created `ai-provider.service.js` layers supporting both Groq and Bedrock API calls.
* Resolved frontend-backend CORS connection blockers and verified quiz generation.
* Successfully ran local mock testing of the integrated platform.
