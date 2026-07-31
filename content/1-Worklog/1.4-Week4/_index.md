---
title: "Week 4 Worklog"
date: 2026-06-22
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

# 4. Database Design & S3 Presigned URL API Integration

### Objectives of the week:

* Design the MongoDB Atlas database schema for LearnSphere.
* Develop backend APIs to support secure direct uploads to S3 from the browser.
* Configure CORS policies to secure cross-origin requests.

### Tasks performed during the week:

| Day | Tasks performed | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| **Monday** | - Design MongoDB Atlas database schemas (Course, Student, Video, Lecture modules, etc.). | 06/22/2026 | 06/22/2026 | https://mongoosejs.com/docs/guide.html |
| **Tuesday** | - Support Dung in writing registration and login APIs, setting up JWT Authentication middleware. | 06/23/2026 | 06/24/2026 | https://jwt.io/introduction |
| **Wednesday** | - Configure MongoDB Atlas IP Access Lists to allow connections only from the backend EC2 server. | 06/24/2026 | 06/24/2026 | https://docs.atlas.mongodb.com/security/ |
| **Thursday** | - Develop a backend API to generate S3 Presigned URLs for direct avatar and thumbnail uploads. | 06/25/2026 | 06/25/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html |
| **Friday** | - Configure CORS allowlist policies on Express backend to allow secure requests from the React frontend. | 06/26/2026 | 06/26/2026 | https://expressjs.com/en/resources/middleware/cors.html |

### Key achievements of week 4:

* Completed 11 Mongoose Schemas covers all business logics of the platform.
* Successfully developed secure upload capability using S3 Presigned URLs.
* Completely resolved cross-origin (CORS) communication errors between Frontend and Backend.
