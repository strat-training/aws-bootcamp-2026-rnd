# m08: Monitoring and Operations

**Schedule:** Day 8 · **Builds on:** `07-m07-compute-fundamentals` · **Feeds into:** `09-m09-aws-services-and-architecture` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee uses CloudWatch metrics, logs and alarms and CloudTrail Event history to investigate simple problems, and states a sensible first troubleshooting check for an S3 AccessDenied response, an EC2 web page that does not load and a failed CloudFormation resource.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 8.1 | CloudWatch metrics, logs and alarms | 0.5 h | CloudWatch Metrics, CPU utilization, CloudWatch Logs, log records, CloudWatch Alarms, threshold, ALARM state | When does the trainee reach for a metric, a log record or an alarm, and what does each one answer? | Steps 1–3: Read metrics and logs and work with an alarm |
| 8.2 | SNS notifications and CloudTrail Event history | 0.5 h | Amazon SNS, topic, subscription, notification, CloudTrail Event history, management events | How does an alarm reach a person through SNS, and what does CloudTrail Event history show that CloudWatch does not? | Step 4 and the optional row: Find a lab action and review notification |
| 8.3 | Troubleshooting order | 0.5 h | identity and permissions, Region, resource configuration, network path, service status, metrics, logs | In what order does the trainee check things when a request fails, and why does the order matter? | Step 5: Work through the three scenarios |
| | **Total** | **1.5 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Provided material | A prepared sample of CloudWatch Logs (or the completed Lambda extension from `cp2`), an instructor-provided metric threshold for the alarm, and the three troubleshooting scenarios. |
| Scope | CloudTrail Event history only: recent management activity in an account and Region. The SNS notification path may be reviewed from the documentation or a prepared topic instead of a full setup. |
| Cost control | Log storage and alarms can incur charges. Alarms and log groups created for the lab are removed when no longer needed. |
| Reference reading | The study material for this self-paced stage: [CloudWatch alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/ConsoleAlarms.html), [CloudTrail Event history](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events-console.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m08: Find metrics, logs and management events

| Step | What the trainee does |
| --- | --- |
| 1 | Reviews EC2 monitoring metrics and identifies CPU utilization. |
| 2 | Opens CloudWatch Logs for a prepared sample, or for the Lambda extension if it was completed. |
| 3 | Creates or inspects a basic CloudWatch alarm using an instructor-provided metric threshold. |
| 4 | Opens CloudTrail Event history and finds a recent action performed during the lab. |
| 5 | Works through short troubleshooting scenarios: an S3 AccessDenied response, an EC2 web page that does not load, and a failed CloudFormation resource. |
| Optional | Reviews how an SNS topic can notify a subscriber when an alarm enters an ALARM state, using the documentation or a prepared topic. A full setup is not required. |
| **Acceptance** | CPU utilization is identified in the EC2 monitoring metrics. CloudWatch Logs records are opened from the prepared sample or the Lambda extension. A basic CloudWatch alarm is created or inspected using the instructor-provided threshold. A recent lab action is found in CloudTrail Event history. The trainee states a sensible first troubleshooting check for each of the three scenarios. The trainee states where to look for metrics, logs and management events. |

## Deliverable

The deliverable contains:

- [ ] Screenshot of the EC2 metrics with CPU utilization identified
- [ ] Screenshot of the CloudWatch Logs records that were opened
- [ ] Screenshot of the alarm and its threshold
- [ ] Screenshot of the CloudTrail Event history entry for the lab action
- [ ] Notes recording the symptom and the first check for each troubleshooting scenario
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which EC2 instance and metrics are reviewed, given that `m07` terminates its instance unless it is designated for reuse? | Step 1 |
| Which prepared log sample and alarm threshold are provided? | Steps 2 and 3 |
| Is a prepared SNS topic provided, or is the review from the documentation only? | The optional row |
| Which check comes first, identity or Region? The topic list in the source module and its beginner troubleshooting sequence give the two in opposite order. | The order taught in lab chunk 8.3 and listed under Troubleshooting order in `m01` |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
