---
title: "Week 7 Worklog"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives: Migration Strategy and Disaster Recovery (Oct 20 – Oct 24)

Migrate workloads from On-Premise to AWS and ensure business continuity.

### Week 7 Objectives:

- Access Security: Eliminate the need for SSH Keys and Port 22 using SSM Session Manager.
- Resource Management: Organize resources using Resource Groups and Tagging Strategy.
- Large-Scale Operations: Execute commands on multiple servers simultaneously without logging into each machine.
- Patching: Automate security patch update process.

### Tasks to be carried out this week:

| Task ID | Day | Work                                                                                                                                           | Start Date | Completion Date | Status    | Reference Material                        |
| ------- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------- | ----------------------------------------- |
| T7.1    | 2   | **VM Migration - Preparation:** <br> - Assess on-premise VMs for migration <br> - Prepare VM Import/Export with AWS CLI                        | 10/20/2025 | 10/20/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.2    | 2   | **Application Migration Service:** <br> - Set up AWS Application Migration Service (MGN) <br> - Install Replication Agent on source server     | 10/20/2025 | 10/21/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.3    | 3   | **Database Migration - DMS Setup:** <br> - Create Database Migration Service endpoints <br> - Configure source and target database connections | 10/21/2025 | 10/22/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.4    | 4   | **DMS - Replication Task:** <br> - Create Replication Task for full load + CDC <br> - Monitor migration progress and data validation           | 10/22/2025 | 10/23/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.5    | 5   | **Disaster Recovery - Backup Plan:** <br> - Set up AWS Backup plan for EC2 and RDS <br> - Configure retention policy and backup window         | 10/23/2025 | 10/24/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T7.6    | 6   | **DR Testing - Pilot Light:** <br> - Design Pilot Light architecture <br> - Test failover scenario and RTO/RPO metrics                         | 10/24/2025 | 10/25/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 7 Achievements:

- **Enhanced Security:**

  - Significantly reduced Attack Surface
  - No admin ports exposed to Internet
  - All access sessions logged in CloudTrail and Session Manager logs
  - Can record sessions for audit

- **Operational Efficiency:**

  - Updated software for entire Autoscaling Group with just a few clicks
  - No need to manage SSH keys for each user
  - Can run scripts on hundreds of servers simultaneously

- **Mindset:**

  - Shifted from "Managing individual servers" to "Fleet Management"
  - Understanding of Zero Trust Network Access
  - No need for bastion host or VPN

- **Skills:**
  - Proficient in SSM Session Manager
  - Understanding of IAM Instance Profile
  - Know how to organize resources with Tags and Resource Groups
  - Use SSM Run Command for automation
