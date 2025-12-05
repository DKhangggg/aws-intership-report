---
title: "Week 4 Worklog"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives: Scalability, Monitoring and Content Distribution (Sep 29 – Oct 03)

Automate system scalability, establish comprehensive monitoring, and optimize global content distribution.

### Tasks Completed This Week:

| Day       | Main Activities                                                                                                                                         | Date                                                                                                                         | Status     | Reference                                 |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------- | --------- | ----------------------------------------- |
| Monday    | **EC2 Auto Scaling**<br>- Create Launch Templates<br>- Configure Auto Scaling Group (Min=2, Max=4)<br>- Set up Target Tracking Scaling Policy (CPU 50%) | 09/29/2025                                                                                                                   | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Tuesday   | **Amazon CloudWatch**<br>- Monitor standard Metrics<br>- Install CloudWatch Agent for Memory Usage<br>- Create Alarms and send notifications via SNS    | 09/30/2025                                                                                                                   | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Wednesday | **Route 53 & CloudFront**<br>- Manage DNS with Route 53<br>- Configure Failover Routing<br>- Deploy CloudFront CDN with OAC                             | 10/01/2025                                                                                                                   | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Thursday  | **AWS CLI & VPC Peering**<br>- Automation with AWS CLI scripts<br>- Set up VPC Peering<br>- Update Route Tables                                         | 10/02/2025                                                                                                                   | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Friday    | **Lambda@Edge**<br>- Deploy edge computing<br>- Write Lambda functions for CloudFront<br>- Implement A/B testing                                        | 10/03/2025                                                                                                                   | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| T4.3      | 3                                                                                                                                                       | **S3 - Public Policy:** <br> - Disable "Block Public Access" <br> - Write Bucket Policy (JSON) allowing s3:GetObject         | 09/30/2025 | 10/01/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.4      | 4                                                                                                                                                       | **RDS - Subnet Group:** <br> - Create DB Subnet Group <br> - Include 2 Private Subnets created in Week 2                     | 10/01/2025 | 10/01/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.5      | 4                                                                                                                                                       | **RDS - Launch DB:** <br> - Launch RDS MySQL (Free Tier) <br> - Disable Multi-AZ <br> - Disable Public Accessibility         | 10/01/2025 | 10/02/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.6      | 5                                                                                                                                                       | **Security - Security Chaining:** <br> - Configure RDS Security Group <br> - Only allow Inbound Port 3306 from Cloud9/EC2 SG | 10/02/2025 | 10/03/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T4.7      | 6                                                                                                                                                       | **Database - Connection Test:** <br> - Use terminal on Cloud9 <br> - Connect MySQL: `mysql -h <endpoint> -u admin -p`        | 10/03/2025 | 10/05/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 4 Achievements:

- **Web:**

  - Static website operational at S3 Endpoint URL
  - Clear understanding of how S3 can host websites without servers
  - Solid grasp of writing Bucket Policy for safe public access

- **Database:**

  - DB instance operating isolated in internal network
  - Cannot access DB directly from Internet (correct security standard)
  - Understanding of RDS Managed Service and its benefits

- **Skills:**

  - Mastered JSON syntax for S3 Policy
  - Understanding of "Security Group Referencing" (nested SG references)
  - Critical technique for building dynamic N-tier architecture

- **Architecture:**
  - Completed preliminary "3-Tier Web Architecture" model:
    - Presentation Tier (S3)
    - Application Tier (Cloud9/EC2)
    - Data Tier (RDS)
  - Understanding of separation of concerns in cloud architecture
