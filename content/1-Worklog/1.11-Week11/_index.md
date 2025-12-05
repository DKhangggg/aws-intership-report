---
title: "Week 11 Worklog"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives: Serverless Architecture (Nov 17 – Nov 21)

Build systems without server management using Lambda, API Gateway, and EventBridge.

### Week 11 Objectives:

- Architecture Audit: Review entire infrastructure based on AWS Well-Architected Tool.
- Quota Management: Check Service Quotas and understand the process for requesting quota increases.
- Resource Cleanup: Find and delete "orphaned" resources.
- Advanced Budgets: Set up AWS Budgets with forecasted breach alerts.

### Tasks to be carried out this week:

| Task ID    | Day | Work                                                                                                                                                        | Start Date | Completion Date | Status    | Reference Material                        |
| ---------- | --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------- | ----------------------------------------- |
| T11.1      | 2   | **EventBridge - Event-Driven:** <br> - Set up EventBridge rules for S3 events <br> - Trigger Lambda on object upload                                        | 11/17/2025 | 11/17/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.2      | 2   | **SQS - Message Queue:** <br> - Create SQS queue for async processing <br> - Configure Dead Letter Queue for failed messages                                | 11/17/2025 | 11/18/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.3      | 3   | **SNS - Pub/Sub Pattern:** <br> - Set up SNS topic with multiple subscribers <br> - Fan-out pattern with SQS and Lambda                                     | 11/18/2025 | 11/18/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.4      | 4   | **AppSync - GraphQL API:** <br> - Create GraphQL schema and resolvers <br> - Real-time subscriptions via WebSocket                                          | 11/19/2025 | 11/19/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.5      | 5   | **X-Ray - Distributed Tracing:** <br> - Enable X-Ray for Lambda and API Gateway <br> - Analyze service map and performance bottlenecks                      | 11/20/2025 | 11/20/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.6      | 6   | **SAM - Serverless Framework:** <br> - Write SAM template for serverless app <br> - Deploy and test with `sam local`                                        | 11/21/2025 | 11/21/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Staff Dashboard (Support Role)**                                                                                                       |            |                 |           |                                           |
| VG11.1     | 2-3 | **Staff Layout & Auth:** <br> - Create separate staff routes from admin <br> - Staff login with role-based permissions <br> - Staff sidebar navigation      | 11/17/2025 | 11/18/2025      | Completed | VoltGo Web Docs                           |
| VG11.2     | 4-5 | **Staff Dashboard:** <br> - Today's tasks & assignments <br> - Station management view (limited permissions) <br> - Vehicle maintenance tracking            | 11/19/2025 | 11/20/2025      | Completed | VoltGo Web Docs                           |
| VG11.3     | 6   | **Staff Operations:** <br> - Report issue form (vehicle/station problems) <br> - Trip support (manual unlock/end trip) <br> - Customer support tickets view | 11/21/2025 | 11/21/2025      | Completed | VoltGo Web Docs                           |

### Week 11 achievements:

- **Risk Report:**

  - Well-Architected Tool indicated High Risk Issue
  - Week 4 Database running Single-AZ
  - If AZ fails, DB loses connection
  - Need to consider Multi-AZ for production

- **Optimization:**

  - Deleted 2 leftover 10GB EBS volumes
  - Save approximately $2/month
  - Released 1 unused Elastic IP
  - Avoid penalty fee of $3.6/month

- **Awareness:**

  - "Good architecture" is a continuous process
  - Not a destination
  - Need regular review and improvement
  - Well-Architected Framework is the guiding principle

- **Governance:**
  - Understanding of Service Quotas and Limits
  - Know how to request quota increase
  - Can forecast when scaling is needed
  - Proactive capacity planning
