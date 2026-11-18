# m10: Infrastructure as Code and CloudFormation Fundamentals

**Schedule:** Day 8 · **Builds on:** `09-m09-aws-services-and-architecture` · **Feeds into:** `11-cp3-one-click-infrastructure` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee reads a short CloudFormation YAML template, identifies its sections and a resource's logical ID and type, deploys a small starter stack, inspects its events, updates it, and deletes it with its resources.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 10.1 | Infrastructure as Code and YAML basics | 0.75 h | Infrastructure as Code, repeatable, version-controlled file, YAML indentation, lists, mappings, key-value structure | What does describing infrastructure in a file give a team that creating it by hand in the Console does not? | Step 1: Open a short YAML template |
| 10.2 | Template anatomy and resources | 1.25 h | Parameters, Resources, Outputs, logical ID, resource type, resource properties, `Ref`, `Fn::GetAtt`, `Fn::Sub` (introductory), resource dependencies, creation order | How does CloudFormation work out the order in which resources are created, and what links one resource to another in a template? | Step 2: Review a sample bucket resource |
| 10.3 | Stack lifecycle | 1.25 h | stack, create, update, delete, stack status, Stack Events | What happens to a stack's resources at each of create, update and delete, and where does the trainee look to see what happened? | Steps 3–6: Deploy, review, update and delete a starter stack |
| 10.4 | Troubleshooting, Change Sets and drift detection | 0.75 h | Stack Events, failed resource, Change Set, drift detection (concepts only) | When a stack fails, where does the trainee look first, and why is a Change Set safer than updating blind? | Step 4: Read the stack events |
| | **Total** | **4.0 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Tools | The CloudFormation Console and a text editor for YAML. |
| Provided material | A short YAML template to read and a very small starter template, for example one that creates an S3 bucket. |
| Scope | Beginner-sized IaC. The trainee is not expected to write a large VPC template or memorize intrinsic functions. Change Sets and drift detection are concepts only. |
| Cleanup | The stack is deleted at the end, and the resources it created are confirmed removed. |
| Reference reading | The study material for this self-paced stage: [CloudFormation template anatomy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html), [EC2 CloudFormation examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-ec2-instance-config.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m10: Read, deploy, update and delete a starter stack

| Step | What the trainee does |
| --- | --- |
| 1 | Opens a short YAML template and identifies its Parameters, Resources and Outputs. |
| 2 | Reviews a sample `AWS::S3::Bucket` resource and identifies its logical ID and type. |
| 3 | Deploys a very small provided starter template, for example an S3 bucket, as a CloudFormation stack. |
| 4 | Reviews the stack status and events. |
| 5 | Changes a simple parameter or tag, updates the stack and observes the result. |
| 6 | Deletes the stack and confirms that the resources created by the stack are removed. |
| **Acceptance** | Parameters, Resources and Outputs are identified in the short YAML template. The logical ID and type of the sample bucket resource are identified. The starter stack is deployed, and its status and events are reviewed. The parameter or tag change is applied as a stack update and the result is observed. The stack is deleted and the resources it created are confirmed removed. |

## Deliverable

The deliverable contains:

- [ ] The short YAML template with its Parameters, Resources and Outputs annotated, and the bucket resource's logical ID and type marked
- [ ] Screenshot of the stack's status and events after the first deployment
- [ ] Screenshot of the stack after the parameter or tag update
- [ ] Evidence that the stack and its created resources were removed
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which short template and starter template are provided? | Lab chunks 10.1 to 10.3 |
| Which parameter or tag is changed for the update? | Step 5 |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
