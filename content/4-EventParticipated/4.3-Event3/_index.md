---
title: "Event 3"
date: 2026-08-01
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Summary Report: "Amazon Bedrock AgentCore - Foundations & Agent Setup" Workshop

### 1. General Event Information
*   **Event Name:** Workshop: Introduction to Amazon Bedrock AgentCore
*   **Date & Time:** 09:00 - 12:00, August 1, 2026
*   **Location:** AWS Vietnam Office Hall, Ho Chi Minh City
*   **Role:** Attendee

---

### 2. Detailed Event Agenda (August 1 - Day 1)

#### 🕐 Time Block: 09:00 – 10:00
*   **Key Focus:** Foundations & Agent Setup
*   **Detailed Content:**
    *   Workshop introduction and alignment on learning outcomes.
    *   **Amazon Bedrock AgentCore Overview**: Exploring the core architecture of AI agents on AWS.
    *   Understanding the 3 primary components:
        *   **Runtime:** The execution environment of the Agent to process inputs and coordinate orchestration.
        *   **Gateway:** Connecting middleware to route conversations and integrate external APIs.
        *   **Identity:** Access management and IAM controls allowing agents to communicate securely with internal resources.
    *   Theoretical overview and resource initialization for the Hands-on Lab.

#### 🕐 Time Block: 10:00 – 11:00
*   **Key Focus:** Hands-on Lab & Integration
*   **Activities:**
    *   **Deploy a basic agent:** Walkthrough on creating and deploying a basic AI agent within AgentCore.
    *   **Connect external tools & Knowledge Bases:** Integrating Action Groups (API extensions) and linking Knowledge Bases to the agent to enable Retrieval-Augmented Generation (RAG).
    *   **Build a Web UI & Cognito Integration:** Creating a modern chat interface (Web UI) and integrating **Amazon Cognito** user pools for secure user authentication.

#### 🕐 Time Block: 11:00 – 12:00
*   **Key Focus:** Testing, Q&A, and Cleanup
*   **Activities:**
    *   Executing end-to-end (E2E) verification of user logins via Cognito and messaging the Bedrock Agent on the frontend.
    *   Technical Q&A session with AWS Solution Architects to troubleshoot implementation roadblocks.
    *   Tearing down initialized cloud resources (Resource Cleanup) on the AWS console to prevent unwanted billing.

---

### 3. Event Verification Photos

Below are the architectural diagram of Bedrock AgentCore and the dashboard of the deployed chat agent with Cognito login, built during the workshop:

![Amazon Bedrock AgentCore Architecture](/images/4-EventParticipated/event3a.jpg)

![Agent Web UI with Amazon Cognito Integration](/images/4-EventParticipated/event3b.jpg)
