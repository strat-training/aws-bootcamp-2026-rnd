# m09: AWS Services and Architecture Overview: Tasks

**Objective:** The trainee explains the purpose of commonly used AWS services (RDS, DynamoDB, SQS, SNS, API Gateway, Elastic Load Balancing, EC2 Auto Scaling, Route 53 and CloudFront) and recommends a service for a simple scenario, at a high level and without provisioning any of them.

> There is no solutions file for this stage. This checklist guides the work, it does not contain it. Source of every task: [`brief.md`](brief.md).

> **Region:** do all of this in Asia Pacific (Singapore), `ap-southeast-1`.

## ID scheme

| Prefix | Meaning | Source in the brief |
| --- | --- | --- |
| `R-<subject>` | Research task | One per row of the Scope table |
| `B-<lab>.<step>` | Build task | One per step of that lab. Optional rows are `B-<lab>.O<n>` and are marked optional |
| `V-<lab>.<n>` | Verify task, checks `DoD-<lab>.<n>` | The n-th clause of that lab's Acceptance row |

## Traceability

| Subject | Research | Build | Verify (DoD) |
| --- | --- | --- | --- |
| 9.1 Data and messaging services | R-9.1 | B-m09.2, B-m09.3 | V-m09.1, V-m09.2 (DoD-m09.1, DoD-m09.2) |
| 9.2 Delivery and scaling services | R-9.2 | B-m09.4, B-m09.5 | V-m09.1, V-m09.3 (DoD-m09.1, DoD-m09.3) |
| 9.3 Service selection | R-9.3 | B-m09.1 | V-m09.4 (DoD-m09.4) |

## Research

- [ ] **R-9.1** (Scope 9.1): Answer in writing: for a simple workload, what makes a relational database or a key-value database the better fit, and when does a team want a queue rather than a notification? Look in the Amazon RDS, Amazon DynamoDB, Amazon SQS and Amazon SNS developer guides.
- [ ] **R-9.2** (Scope 9.2): Answer in writing: how do a load balancer and an Auto Scaling group together support a web application, and where do Route 53 and CloudFront sit in front of it? Look in the Elastic Load Balancing, EC2 Auto Scaling, Amazon Route 53, Amazon CloudFront and Amazon API Gateway documentation.
- [ ] **R-9.3** (Scope 9.3): Answer in writing: which questions do you ask about a requirement before choosing a service? Look at the overview pages of the service documentation for the services in the scope table.

## Build

### Lab m09: Match requirements to services

- [ ] **B-m09.1** (Lab m09 step 1): Match a simple workload requirement to a likely AWS service.
- [ ] **B-m09.2** (Lab m09 step 2): Compare RDS and DynamoDB at a basic use-case level.
- [ ] **B-m09.3** (Lab m09 step 3): Compare SQS and SNS using a queue-versus-notification scenario.
- [ ] **B-m09.4** (Lab m09 step 4): Explain how an Application Load Balancer and an Auto Scaling group can support a web application.
- [ ] **B-m09.5** (Lab m09 step 5): Describe how Route 53 and CloudFront can be used in front of an application or website.

## Verify

### Lab m09

- [ ] **V-m09.1** (checks DoD-m09.1): Check the purpose of each service in the scope table (RDS, DynamoDB, SQS, SNS, API Gateway, Elastic Load Balancing, EC2 Auto Scaling, Route 53 and CloudFront) is explained. *Validates R-9.1, R-9.2, B-m09.2, B-m09.3, B-m09.4, B-m09.5.*
- [ ] **V-m09.2** (checks DoD-m09.2): Check RDS is compared with DynamoDB, and SQS with SNS, at a basic use-case level. *Validates R-9.1, B-m09.2, B-m09.3.*
- [ ] **V-m09.3** (checks DoD-m09.3): Check there is a description of how a load balancer and an Auto Scaling group, and Route 53 and CloudFront, can sit in front of a web application. *Validates R-9.2, B-m09.4, B-m09.5.*
- [ ] **V-m09.4** (checks DoD-m09.4): Check a basic service recommendation is made for a simple scenario. *Validates R-9.3, B-m09.1.*
