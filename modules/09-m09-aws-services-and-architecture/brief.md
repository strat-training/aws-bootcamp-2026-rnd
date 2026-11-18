# m09: AWS Services and Architecture Overview

**Schedule:** Day 8 · **Builds on:** `08-m08-monitoring-and-operations` · **Feeds into:** `10-m10-iac-and-cloudformation` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee explains the purpose of commonly used AWS services (RDS, DynamoDB, SQS, SNS, API Gateway, Elastic Load Balancing, EC2 Auto Scaling, Route 53 and CloudFront) and recommends a service for a simple scenario, at a high level and without provisioning any of them.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 9.1 | Data and messaging services | 0.5 h | Amazon RDS, managed relational database, Amazon DynamoDB, managed NoSQL key-value and document database, Amazon SQS, message queue, decoupling, Amazon SNS, publish/subscribe, notification | For a simple workload, what makes a relational database or a key-value database the better fit, and when does a team want a queue rather than a notification? | Steps 2–3: Compare RDS with DynamoDB and SQS with SNS |
| 9.2 | Delivery and scaling services | 0.5 h | Amazon API Gateway, Elastic Load Balancing, Application Load Balancer, EC2 Auto Scaling, Auto Scaling group, Amazon Route 53, DNS and domain routing, Amazon CloudFront, content delivery and caching | How do a load balancer and an Auto Scaling group together support a web application, and where do Route 53 and CloudFront sit in front of it? | Steps 4–5: Explain the web application and front-door patterns |
| 9.3 | Service selection | 0.25 h | requirement before service, workload requirement, service recommendation | Which questions does the trainee ask about a requirement before choosing a service? | Step 1: Match a requirement to a service |
| | **Total** | **1.25 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Provisioning | None is required. NAT Gateways, load balancers, RDS databases and multi-AZ deployments are avoided in the required labs because they are not needed to meet the learning outcomes. |
| Provided material | Simple workload requirements and the queue-versus-notification scenario, supplied with the exercise. |
| Format | A self-paced written exercise. The trainee's answers are written down, because the stage has no console output to show. |
| Reference reading | The study material for this self-paced stage: [Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html), [Amazon DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html), [Amazon SQS](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html), [Amazon SNS](https://docs.aws.amazon.com/sns/latest/dg/welcome.html), [Amazon API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html), [Elastic Load Balancing](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-load-balancing.html), [Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html), [Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html), [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m09: Match requirements to services

| Step | What the trainee does |
| --- | --- |
| 1 | Matches a simple workload requirement to a likely AWS service. |
| 2 | Compares RDS and DynamoDB at a basic use-case level. |
| 3 | Compares SQS and SNS using a queue-versus-notification scenario. |
| 4 | Explains how an Application Load Balancer and an Auto Scaling group can support a web application. |
| 5 | Describes how Route 53 and CloudFront can be used in front of an application or website. |
| **Acceptance** | The trainee explains the purpose of each service in the scope table. The trainee compares RDS with DynamoDB and SQS with SNS at a basic use-case level. The trainee describes how a load balancer and an Auto Scaling group, and Route 53 and CloudFront, can sit in front of a web application. The trainee makes a basic service recommendation for a simple scenario. |

## Deliverable

The deliverable contains:

- [ ] Written answers to the five lab steps
- [ ] The service recommendation for the instructor's scenario, with the requirement it answers
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which workload requirements and scenarios are given to the trainee? | Steps 1 and 3 |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
