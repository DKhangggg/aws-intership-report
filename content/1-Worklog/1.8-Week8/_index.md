---
title: "Week 8 Worklog"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives: Cost Optimization and Advanced Networking (Oct 27 – Oct 31)

Control cloud cash flow (FinOps) and large-scale network connectivity.

### Week 8 Objectives:

- Infrastructure Automation: Recreate network architecture (VPC) and servers (EC2) with code.
- Understanding Essence: Master CloudFormation structure (Parameters, Resources, Outputs).
- Modern Tools: Get familiar with AWS CDK and the cdk init, cdk synth, cdk deploy workflow.
- Lifecycle Management: Practice clean deletion (Destroy) and recreation (Deploy) of entire stack in minutes.

### Tasks to be carried out this week:

| Task ID    | Day | Work                                                                                                                                                     | Start Date | Completion Date | Status    | Reference Material                        |
| ---------- | --- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------- | ----------------------------------------- |
| T8.1       | 2   | **Cost Explorer - Deep Dive:** <br> - Analyze costs by Service and Region <br> - Identify top 5 most expensive services                                  | 10/27/2025 | 10/27/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.2       | 2   | **Compute Optimizer - Right-Sizing:** <br> - Review recommendations for EC2 instances <br> - Apply right-sizing suggestions (downgrade over-provisioned) | 10/27/2025 | 10/28/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.3       | 3   | **Savings Plans - Analysis:** <br> - Evaluate Savings Plans vs Reserved Instances <br> - Purchase Compute Savings Plan 1-year commitment                 | 10/28/2025 | 10/28/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.4       | 4   | **Budgets - Advanced Alerts:** <br> - Create Budget with forecast-based alerts <br> - Configure SNS for multi-threshold notifications                    | 10/29/2025 | 10/29/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.5       | 5   | **Transit Gateway - Hub Architecture:** <br> - Set up Transit Gateway as hub <br> - Connect multiple VPCs through TGW                                    | 10/30/2025 | 10/30/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.6       | 5   | **TGW - Route Tables:** <br> - Configure TGW Route Tables for isolation <br> - Test connectivity between VPC attachments                                 | 10/30/2025 | 10/31/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T8.7       | 6   | **Cost Optimization Report:** <br> - Compile recommendations and savings achieved <br> - Plan FinOps strategy for next month                             | 10/31/2025 | 10/31/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Rental Flow & QR Scanner**                                                                                                          |            |                 |           |                                           |
| VG8.1      | 2-3 | **QR Code Scanner:** <br> - Implement QR Scanner with expo-camera <br> - Request camera permission <br> - Parse QR code and extract vehicle ID           | 10/27/2025 | 10/28/2025      | Completed | VoltGo Internal Docs                      |
| VG8.2      | 4-5 | **Unlock Flow:** <br> - Vehicle preview screen before unlock <br> - Confirm unlock action <br> - API call to unlock vehicle and start trip               | 10/29/2025 | 10/30/2025      | Completed | VoltGo API Docs                           |
| VG8.3      | 6   | **Active Trip Screen:** <br> - Real-time timer showing trip duration <br> - Live cost calculation <br> - End trip button with confirmation               | 10/31/2025 | 10/31/2025      | Completed | VoltGo Figma Design                       |

### Week 8 achievements:

- **Speed:**

  - Can rebuild entire network environment in just 2 minutes running commands
  - Instead of 30 minutes of manual clicking
  - Minimizes human errors

- **Control:**

  - Infrastructure code stored in Git
  - Review change history (Who modified the Subnet? Why?)
  - Code review for infrastructure changes
  - Version control for infrastructure

- **Experience:**

  - CDK is intuitive and requires less code than pure CloudFormation
  - Thanks to high-level Constructs (L2, L3)
  - Has type checking and autocomplete
  - Easy to test infrastructure code

- **Skills:**

  - Understanding of Infrastructure as Code (IaC)
  - Solid grasp of CloudFormation template structure
  - Proficient in AWS CDK with TypeScript
  - Know how to use Drift Detection

- Used AWS CLI to perform basic operations such as:

  - Check account & configuration information
  - Retrieve the list of regions
  - View EC2 service
  - Create and manage key pairs
  - Check information about running services
  - ...

- Acquired the ability to connect between the web interface and CLI to manage AWS resources in parallel.
- ...
