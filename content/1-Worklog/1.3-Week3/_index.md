---
title: "Week 3 Worklog"
date: 2026-09-28
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---


### Week 3 Objectives:

* Understand application modernization strategies and principles for decomposing monolithic architectures into microservices.
* Master decentralized data persistence patterns (Database-per-Service, Polyglot Persistence, Eventual Consistency).
* Learn standard microservices architectures on AWS using Amazon API Gateway, compute services (Lambda, ECS), and decoupled messaging.
* Review core, production-grade AWS services essential for designing and operating real-world cloud applications.
* Analyze Ownword's core architecture, design the target AWS Serverless blueprint, optimize the MVP scope, and formulate strict cost-defense guardrails.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Decomposing Monoliths into Microservices: <br>&emsp; + Learn decomposition strategies and identifying business capabilities <br>&emsp; + Domain-Driven Design (DDD) & Bounded Contexts <br>&emsp; + Strangler Fig pattern for incremental migration <br>&emsp; + Decoupling application logic and monolithic databases | 28/09/2026 | 28/09/2026 | <https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-decomposing-monoliths/introduction.html> |
| 3   | - Decentralized Data Architecture & Modernizing Data Persistence: <br>&emsp; + Database-per-service pattern & distributed data ownership <br>&emsp; + Principles of Polyglot Persistence (RDS/Aurora, DynamoDB, ElastiCache, DocumentDB) <br>&emsp; + Handling Eventual Consistency and Saga pattern <br>&emsp; + Data migration & synchronization patterns (CQRS, Transactional Outbox, CDC via AWS DMS) | 29/09/2026 | 29/09/2026 | <https://docs.aws.amazon.com/whitepapers/latest/microservices-on-aws/data-store.html> <br> <https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-data-persistence/introduction.html> |
| 4   | - Microservices Architecture & Core Production AWS Services: <br>&emsp; + API Gateway entry routing (Rate Limiting, Auth, Routing) <br>&emsp; + Compute layers: Serverless (AWS Lambda) & Containers (Amazon ECS/Fargate) <br>&emsp; + Asynchronous messaging & event decoupling with Amazon SQS, SNS & EventBridge <br>&emsp; + Essential AWS production stack: Edge/CDN (Route 53, CloudFront), Security (WAF, Cognito) | 30/09/2026 | 30/09/2026 | <https://docs.aws.amazon.com/whitepapers/latest/microservices-on-aws/simple-microservices-architecture-on-aws.html> <br> <https://youtu.be/n28iOV_Y_tQ?si=p4dBo5Qh_cATC62E> |
| 5   | - Ownword Tech Stack Analysis & Architecture Modernization: <br>&emsp; + Analyzed current tech stack: Decoded Ownword's core technologies (Next.js, D1, Drizzle, Gemini API) from an AI development perspective <br>&emsp; + Drafted architecture diagrams: Created Mermaid visualization diagrams for the existing Cloudflare edge setup and the target AWS Serverless architecture <br>&emsp; + Optimized MVP scope: Evaluated architecture documentation to intentionally exclude non-essential services (S3, SQS, EventBridge, CloudFront) | 01/10/2026 | 01/10/2026 | <https://docs.aws.amazon.com/serverless/> |
| 6   | - Cost Guardrails & Deployment Strategy Formulation: <br>&emsp; + Set cost guardrails: Formulated a strict $1.00/month AWS Budgets and CloudWatch Billing Alarm setup to prevent accidental charges <br>&emsp; + Verified Free Tier pricing: Broken down AWS Free Tier allowances and safe configurations for Amplify, Cognito, Lambda, API Gateway, and RDS PostgreSQL <br>&emsp; + Summarized deployment strategy: Compiled technical breakdown and cost-defense plan into the final proposal and architecture document | 02/10/2026 | 02/10/2026 | <https://aws.amazon.com/free/> <br> <https://aws.amazon.com/aws-cost-management/aws-budgets/> |


### Week 3 Achievements:

* **Microservices Architecture & Modernization**: Mastered strategies for decomposing monolithic applications using Domain-Driven Design (DDD), Bounded Contexts, and the Strangler Fig pattern for incremental, low-risk migration.
* **Decentralized Data Management**: Understood the Database-per-Service principle to maintain loose coupling across microservices and eliminate shared-database bottlenecks.
* **Polyglot Persistence**: Gained proficiency in selecting purpose-built AWS databases (Amazon DynamoDB, Amazon RDS/Aurora, Amazon ElastiCache) matching specific access patterns, workloads, and performance requirements.
* **Distributed Consistency & Transactions**: Learned techniques to manage eventual consistency, distributed workflows, and transactional integrity using the Saga pattern, Event Sourcing, and Change Data Capture (CDC).
* **AWS Microservices Architecture**: Grasped end-to-end design patterns combining Amazon API Gateway as a centralized entry point with scalable compute options (AWS Lambda, Amazon ECS/Fargate) and asynchronous messaging (Amazon SQS, SNS).
* **Core Production AWS Services**: Gained a solid understanding of the essential ~10% of AWS services most commonly used in real-world production workloads and how they interconnect into an enterprise-ready architecture.
* **Ownword Modernization & Architecture Blueprint**: Decoded Ownword's full-stack AI technologies (Next.js, Cloudflare D1, Drizzle, Gemini API) and drafted comprehensive Mermaid diagrams mapping the migration to an AWS Serverless architecture.
* **Strict Cost Defense & MVP Optimization**: Proactively formulated a defensive $1.00/month AWS Budgets and CloudWatch Billing Alarm system, optimized MVP scope by deferring non-critical services, validated Free Tier usage boundaries, and packaged the complete deployment strategy.
