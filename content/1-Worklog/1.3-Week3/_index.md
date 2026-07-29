---
title: "Week 3 Worklog"
date: 2026-07-25
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

# Week 3 - Amazon S3 Storage Integration

### Week Objectives:

* Configure Amazon S3 SDK inside LearnSphere Backend for media assets.
* Implement secure uploading using S3 Presigned URLs.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Studying S3 architecture: Presigned URLs vs direct uploads. | 29/06/2026 | 29/06/2026 |
| 2 | Writing file upload helper logic in backend file service. | 30/06/2026 | 30/06/2026 |
| 3 | Implementing presigned GET and PUT operations using AWS SDK. | 01/07/2026 | 01/07/2026 |
| 4 | Adding file type validation rules (e.g. video/mp4, image/jpeg). | 02/07/2026 | 02/07/2026 |
| 5 | Verifying local S3 upload-download lifecycle using SDK. | 03/07/2026 | 03/07/2026 |

### Week Achievements:

* Successfully integrated AWS SDK v3 S3 client.
* Completed `createPresignedUpload` and `createPresignedDownload` service APIs.
* Prevented public bucket exposure by enforcing short-lived S3 signature URLs.
