---
title: "Week 9 Worklog"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives: Container Technology (Nov 03 – Nov 07)

Deploy Docker applications on ECS with Fargate for optimization and robust management.

### Week 9 Objectives:

- Network Transparency: Collect and analyze network traffic to detect unusual connections.
- Log Querying: Use CloudWatch Logs Insights to run queries on massive log data.
- Cost Optimization: Identify wasted resources and perform "Right Sizing".
- Billing Permissions: Configure Billing access permissions for IAM accounts.

### Tasks to be carried out this week:

| Task ID    | Day | Work                                                                                                                                                             | Start Date | Completion Date | Status    | Reference Material                        |
| ---------- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------- | ----------------------------------------- |
| T9.1       | 2   | **Docker - Containerization:** <br> - Write optimized Dockerfile with Multi-stage build <br> - Build image and test locally                                      | 11/03/2025 | 11/03/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.2       | 2   | **ECR - Image Registry:** <br> - Create ECR Repository <br> - Push Docker image to ECR with tag versioning                                                       | 11/03/2025 | 11/04/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.3       | 3   | **ECS Fargate - Task Definition:** <br> - Define Task with CPU/RAM requirements <br> - Configure container port mappings                                         | 11/04/2025 | 11/04/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.4       | 4   | **ECS - Service Deployment:** <br> - Create ECS Cluster and Service <br> - Launch Type: Fargate (serverless containers)                                          | 11/05/2025 | 11/05/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.5       | 5   | **Load Balancing - ALB Integration:** <br> - Integrate ECS Service with Application Load Balancer <br> - Configure Health Check and Target Group                 | 11/06/2025 | 11/06/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.6       | 6   | **Auto Scaling - Container Level:** <br> - Set up Service Auto Scaling based on CPU <br> - Test scaling behavior under increased load                            | 11/07/2025 | 11/07/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Trips & Messages Tabs**                                                                                                                     |            |                 |           |                                           |
| VG9.1      | 2-3 | **Trips Tab - History:** <br> - Fetch trip history from API <br> - FlatList displaying past trips <br> - Trip card component with details (date, duration, cost) | 11/03/2025 | 11/04/2025      | Completed | VoltGo API Docs                           |
| VG9.2      | 4-5 | **Trip Detail Screen:** <br> - Show full trip information <br> - Map route visualization <br> - Invoice/Receipt generation                                       | 11/05/2025 | 11/06/2025      | Completed | VoltGo Figma Design                       |
| VG9.3      | 6   | **Messages Tab:** <br> - System notifications list <br> - Support chat UI skeleton <br> - Unread badge indicator                                                 | 11/07/2025 | 11/07/2025      | Completed | VoltGo Figma Design                       |

### Week 9 achievements:

- **Investigation:**

  - Identified which IP addresses are attempting to scan SSH port
  - Discovered attack patterns
  - Can trace network path

- **Savings:**

  - Compute Optimizer indicated instances running below 5% CPU
  - Confirmed t3.micro is appropriate or can be consolidated
  - Discovered unused resources

- **Skills:**

  - Proficient in Logs Insights query syntax
  - Critical skill for rapid troubleshooting
  - Understanding of VPC Flow Logs format

- **FinOps:**
  - Know how to analyze costs from multiple dimensions
  - Understanding of Cost Allocation Tags
  - Can forecast monthly costs
