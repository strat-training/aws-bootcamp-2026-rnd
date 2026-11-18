# m08: Monitoring and Operations: Tasks

**Objective:** The trainee uses CloudWatch metrics, logs and alarms and CloudTrail Event history to investigate simple problems, and states a sensible first troubleshooting check for an S3 AccessDenied response, an EC2 web page that does not load and a failed CloudFormation resource.

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
| 8.1 CloudWatch metrics, logs and alarms | R-8.1 | B-m08.1, B-m08.2, B-m08.3 | V-m08.1, V-m08.2, V-m08.3 (DoD-m08.1, DoD-m08.2, DoD-m08.3) |
| 8.2 SNS notifications and CloudTrail Event history | R-8.2 | B-m08.4, B-m08.O1 | V-m08.4 (DoD-m08.4) |
| 8.3 Troubleshooting order | R-8.3 | B-m08.5 | V-m08.5, V-m08.6 (DoD-m08.5, DoD-m08.6) |

## Research

- [ ] **R-8.1** (Scope 8.1): Answer in writing: when do you reach for a metric, a log record or an alarm, and what does each one answer? Look in the CloudWatch documentation on metrics, logs and alarms.
- [ ] **R-8.2** (Scope 8.2): Answer in writing: how does an alarm reach a person through SNS, and what does CloudTrail Event history show that CloudWatch does not? Look in the SNS documentation and the CloudTrail Event history documentation.
- [ ] **R-8.3** (Scope 8.3): Answer in writing: in what order do you check things when a request fails, and why does the order matter? Look in the AWS documentation for the services in the three scenarios of B-m08.5, and finalise after working through them.

## Build

### Lab m08: Find metrics, logs and management events

- [ ] **B-m08.1** (Lab m08 step 1): Review EC2 monitoring metrics and identify CPU utilization.
- [ ] **B-m08.2** (Lab m08 step 2): Open CloudWatch Logs for a prepared sample, or for the Lambda extension if it was completed.
- [ ] **B-m08.3** (Lab m08 step 3): Create or inspect a basic CloudWatch alarm using an instructor-provided metric threshold.
- [ ] **B-m08.4** (Lab m08 step 4): Open CloudTrail Event history and find a recent action performed during the lab.
- [ ] **B-m08.5** (Lab m08 step 5): Work through the short troubleshooting scenarios: an S3 AccessDenied response, an EC2 web page that does not load, and a failed CloudFormation resource.
- [ ] **B-m08.O1** (optional, Lab m08 optional row): Review how an SNS topic can notify a subscriber when an alarm enters an ALARM state. Use the documentation or a prepared topic. A full setup is not required.

## Verify

### Lab m08

- [ ] **V-m08.1** (checks DoD-m08.1): Check CPU utilization is identified in the EC2 monitoring metrics. *Validates R-8.1, B-m08.1.*
- [ ] **V-m08.2** (checks DoD-m08.2): Check CloudWatch Logs records are opened from the prepared sample or the Lambda extension. *Validates R-8.1, B-m08.2.*
- [ ] **V-m08.3** (checks DoD-m08.3): Check a basic CloudWatch alarm is created or inspected using the instructor-provided threshold. *Validates R-8.1, B-m08.3.*
- [ ] **V-m08.4** (checks DoD-m08.4): Check a recent lab action is found in CloudTrail Event history. *Validates R-8.2, B-m08.4.*
- [ ] **V-m08.5** (checks DoD-m08.5): Check a sensible first troubleshooting check is stated for each of the three scenarios. *Validates R-8.3, B-m08.5.*
- [ ] **V-m08.6** (checks DoD-m08.6): Check where to look for metrics, logs and management events is stated. *Validates R-8.1, R-8.2, B-m08.1, B-m08.2, B-m08.4.*
