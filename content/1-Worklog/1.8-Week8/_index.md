---
title: "Week 8 Worklog"
date: 2026-07-20
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

# 8. CloudWatch Logs Integration & Amazon SNS Alarms Setup

### Objectives of the week:

* Configure centralized container logs streaming to AWS CloudWatch for debugging.
* Set up automated email alerts for server failures and high resource utilization.
* Optimize S3 bucket storage classes and objects lifecycles.

### Tasks performed during the week:

| Day | Tasks performed | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| **Monday** | - Configure Docker logging driver on EC2 to stream container console output to CloudWatch Logs. | 07/20/2026 | 07/20/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html |
| **Tuesday** | - Create CloudWatch Alarms for EC2 `CPUUtilization` and `StatusCheckFailed` metrics. | 07/21/2026 | 07/22/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| **Thursday** | - Set up an Amazon SNS Topic and subscribe administrator email addresses to receive alerts. | 07/24/2026 | 07/24/2026 | https://docs.aws.amazon.com/sns/latest/dg/welcome.html |
| **Friday** | - Configure S3 Lifecycle Policies to automatically delete temporary files or transition old assets. | 07/24/2026 | 07/24/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html |

### Key achievements of week 8:

* Backend container logs are streamed to CloudWatch Logs for centralized management and debugging.
* Verified automated alert system sending real-time emails during simulated EC2 failures.
* Optimized S3 storage costs by setting up automatic object expiration rules.
