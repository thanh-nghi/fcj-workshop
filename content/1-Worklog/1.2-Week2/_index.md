---
title: "Week 2 Worklog"
date: 2026-09-21
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Manage costs and set up budgets to monitor AWS resources using AWS Budgets.
* Monitor infrastructure and applications comprehensively with Amazon CloudWatch (Metrics, Logs, Alarms, Dashboards).
* Deploy Amazon RDS relational databases integrated with EC2 web servers and Node.js applications.
* Build High Availability and Auto Scaling architectures using Elastic Load Balancing (ELB) and Auto Scaling Group (ASG).
* Configure Hybrid DNS architecture connecting On-Premise Active Directory and Amazon Route 53 Resolver.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Cost Management with AWS Budgets: <br>&emsp; + Create Cost Budget to control recurring costs <br>&emsp; + Create Usage Budget to monitor resource usage hours <br>&emsp; + Learn about Reservation Budget & Savings Plans Budget <br>&emsp; + Set up Email alert thresholds <br>&emsp; + Perform Budget resource cleanup | 21/09/2026 | 21/09/2026 | <https://000007.awsstudygroup.com/> |
| 2 | - System Monitoring with Amazon CloudWatch: <br>&emsp; + Initialize lab infrastructure using CloudFormation Template <br>&emsp; + Visualize Metrics using Search Expressions & Math Expressions <br>&emsp; + Configure automated Dynamic Labels <br>&emsp; + Manage CloudWatch Logs & query with Logs Insights Engine <br>&emsp; + Create Metric Filters & configure CloudWatch Alarms <br>&emsp; + Build centralized CloudWatch Dashboard | 22/09/2026 | 22/09/2026 | <https://000008.awsstudygroup.com/> |
| 3 | - Deploy Amazon RDS Database & Web Application: <br>&emsp; + Set up VPC network infrastructure, Security Groups (ec2-sg, rds-sg) & DB Subnet Group <br>&emsp; + Launch Amazon RDS MySQL Instance with Multi-AZ configuration <br>&emsp; + Launch EC2 Amazon Linux 2023 web server and SSH via MobaXterm <br>&emsp; + Deploy Node.js Web Application, manage background processes using PM2 <br>&emsp; + Initialize MySQL database and perform CRUD operations <br>&emsp; + Practice Backup, Snapshots, and Database Restore workflow | 23/09/2026 | 24/09/2026 | <https://000005.awsstudygroup.com/> |
| 4 | - Auto Scaling with Load Balancer & Auto Scaling Group: <br>&emsp; + Set up Multi-AZ VPC, Security Groups (fcaj-sg, fcaj-db-sg) <br>&emsp; + Create AMI from EC2 Instance and configure Launch Template <br>&emsp; + Create Application Load Balancer (ALB) & Target Group <br>&emsp; + Configure Auto Scaling Group (ASG) integrated with ALB and SNS Notifications <br>&emsp; + Test scaling strategies: Manual Scaling, Scheduled Scaling, Dynamic Scaling (Target Tracking) & Predictive Scaling using JMeter | 25/09/2026 | 25/09/2026 | <https://000006.awsstudygroup.com/> |
| 5 | - Set Up Hybrid DNS Architecture with Route 53 Resolver: <br>&emsp; + Deploy network infrastructure using AWS Quick Start & CloudFormation <br>&emsp; + Initialize AWS Managed Microsoft Active Directory simulating On-premise DNS <br>&emsp; + Configure Route 53 Outbound Endpoints & Inbound Endpoints <br>&emsp; + Set up Route 53 Resolver Rules for domain query forwarding <br>&emsp; + Test bidirectional domain resolution between On-premise and Route 53 <br>&emsp; + Clean up all deployed resources | 26/09/2026 | 26/09/2026 | <https://000010.awsstudygroup.com/> |

### Week 2 Achievements:

* **Hands-on AWS Budgets cost management tools**: Learned how to set up various budget types (Cost, Usage, RI, Savings Plans) and configure automated email alerts to proactively control operational costs on AWS.
* **Hands-on Amazon CloudWatch**: Gained proficiency in querying deep logs with CloudWatch Logs Insights, creating Metric Filters from error logs, setting up Alarms, and building centralized dashboards.
* **Deployed Web Applications with Amazon RDS**: Mastered the process of creating multi-AZ VPCs, separating Security Groups between Web Tier and Database Tier, launching RDS MySQL Multi-AZ instances, and running Node.js background apps with PM2.
* **Data Backup & Restoration**: Proficiently managed DB Snapshots and restored RDS databases to a desired point in time (Point-in-time recovery).
* **Automated Infrastructure Expansion with ELB & ASG**: Successfully built high-availability systems, distributing traffic via Application Load Balancers and automatically adjusting EC2 instance counts based on actual workload demands.
* **Understood Various Scaling Strategies**: Compared and evaluated performance across different scaling approaches: Manual Scaling, Scheduled Scaling, Dynamic Scaling (Target Tracking), and Predictive Scaling through load-testing simulations using JMeter.
* **Built Hybrid DNS Infrastructure**: Successfully configured Inbound/Outbound Endpoints and Resolver Rules on Route 53 Resolver, enabling seamless cross-domain resolution between On-premise AD and AWS Cloud resources.