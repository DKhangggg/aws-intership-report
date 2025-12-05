---
title: "Week 6 Worklog"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives: Multi-Layer Security Architecture (Oct 13 – Oct 17)

Build a digital fortress to protect data and applications from modern cyber threats.

### Week 6 Objectives:

- Observability: Build a centralized Dashboard to monitor system health.
- Proactive Alerts: Set up alerting system via Email/SMS when resources encounter issues.
- Automation: Write Lambda function (Python/Node.js) to interact with AWS resources.
- Scheduling: Use Amazon EventBridge to trigger Lambda on schedule (Cron job).

### Tasks to be carried out this week:

| Task ID    | Day | Work                                                                                                                                                                   | Start Date | Completion Date | Status    | Reference Material                        |
| ---------- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------- | ----------------------------------------- |
| T6.1       | 2   | **AWS WAF - Web Application Firewall:** <br> - Create Web ACL and attach to ALB <br> - Configure rules to block SQL Injection and XSS attacks                          | 10/13/2025 | 10/13/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.2       | 2   | **WAF - Rate Limiting:** <br> - Set up Rate-based rule <br> - Block IPs sending over 100 requests/5 minutes for DDoS protection                                        | 10/13/2025 | 10/14/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.3       | 3   | **KMS - Key Management:** <br> - Create Customer Managed Key (CMK) <br> - Configure Key Policy to control encryption/decryption permissions                            | 10/14/2025 | 10/14/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.4       | 4   | **KMS - Encryption Integration:** <br> - Enable encryption for EBS Volume using CMK <br> - Activate S3 Bucket encryption with KMS key                                  | 10/15/2025 | 10/15/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.5       | 4   | **Secrets Manager - Setup:** <br> - Store RDS password in Secrets Manager <br> - Configure automatic rotation with Lambda                                              | 10/15/2025 | 10/16/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.6       | 5   | **GuardDuty - Threat Detection:** <br> - Enable GuardDuty to analyze CloudTrail/VPC Flow Logs <br> - Configure EventBridge to send alerts when threats detected        | 10/16/2025 | 10/16/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.7       | 6   | **Cognito - User Authentication:** <br> - Create User Pool for web application <br> - Test user registration/login functionality                                       | 10/17/2025 | 10/17/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Authentication & Core UI**                                                                                                                        |            |                 |           |                                           |
| VG6.1      | 2-3 | **Auth Screens:** <br> - Implement Login screen (NativeWind styling) <br> - Implement Register screen <br> - OTP Verification screen                                   | 10/13/2025 | 10/14/2025      | Completed | VoltGo Figma Design                       |
| VG6.2      | 4-5 | **Auth Context & Storage:** <br> - Create AuthContext with React Context API <br> - Implement SecureStore for token management <br> - Auth guard logic in \_layout.tsx | 10/15/2025 | 10/16/2025      | Completed | VoltGo Internal Docs                      |
| VG6.3      | 6   | **Tab Navigation:** <br> - Setup 5 tabs: Explore, Messages, Trips, Support, Profile <br> - Dynamic Profile tab (Guest vs User)                                         | 10/17/2025 | 10/17/2025      | Completed | VoltGo Internal Docs                      |

### Week 6 achievements:

- **Vision:**

  - Real-time view of system performance
  - No longer need to SSH into each machine to run `top` command
  - Centralized dashboard for all resources

- **Response:**

  - Receive immediate email alert when CPU is high
  - Re-tested with Stress Test from Week 5
  - Alert system works well

- **FinOps:**

  - Automatically shut down Development environment at end of day
  - Save approximately 65% EC2 cost (8h instead of 24h)
  - Lambda runs at nearly $0 cost

- **Skills:**
  - Write Lambda function with Python and boto3
  - Understanding of Event-Driven Architecture
  - Configure EventBridge (CloudWatch Events)
  - Integrate SNS for notification system
