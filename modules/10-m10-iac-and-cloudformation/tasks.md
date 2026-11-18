# m10: Infrastructure as Code and CloudFormation Fundamentals: Tasks

**Objective:** The trainee reads a short CloudFormation YAML template, identifies its sections and a resource's logical ID and type, deploys a small starter stack, inspects its events, updates it, and deletes it with its resources.

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
| 10.1 Infrastructure as Code and YAML basics | R-10.1 | B-m10.1 | V-m10.1 (DoD-m10.1) |
| 10.2 Template anatomy and resources | R-10.2 | B-m10.2 | V-m10.2 (DoD-m10.2) |
| 10.3 Stack lifecycle | R-10.3 | B-m10.3, B-m10.5, B-m10.6 | V-m10.3, V-m10.4, V-m10.5 (DoD-m10.3, DoD-m10.4, DoD-m10.5) |
| 10.4 Troubleshooting, Change Sets and drift detection | R-10.4 | B-m10.4 | V-m10.3 (DoD-m10.3) |

## Research

- [ ] **R-10.1** (Scope 10.1): Answer in writing: what does describing infrastructure in a file give a team that creating it by hand in the Console does not? Look in the AWS CloudFormation documentation on what CloudFormation is and the benefits it lists.
- [ ] **R-10.2** (Scope 10.2): Answer in writing: how does CloudFormation work out the order in which resources are created, and what links one resource to another in a template? Look in the CloudFormation user guide sections on template anatomy and resource dependencies.
- [ ] **R-10.3** (Scope 10.3): Answer in writing: what happens to a stack's resources at each of create, update and delete, and where do you look to see what happened? Look in the CloudFormation documentation on the stack lifecycle and on viewing stack events.
- [ ] **R-10.4** (Scope 10.4): Answer in writing: when a stack fails, where do you look first, and why is a Change Set safer than updating blind? Look in the CloudFormation documentation on troubleshooting and on Change Sets. Change Sets and drift detection are concepts only.

## Build

### Lab m10: Read, deploy, update and delete a starter stack

- [ ] **B-m10.1** (Lab m10 step 1): Open a short YAML template and identify its Parameters, Resources and Outputs.
- [ ] **B-m10.2** (Lab m10 step 2): Review a sample `AWS::S3::Bucket` resource and identify its logical ID and type.
- [ ] **B-m10.3** (Lab m10 step 3): Deploy a very small provided starter template, for example an S3 bucket, as a CloudFormation stack.
- [ ] **B-m10.4** (Lab m10 step 4): Review the stack status and events.
- [ ] **B-m10.5** (Lab m10 step 5): Change a simple parameter or tag, update the stack and observe the result.
- [ ] **B-m10.6** (Lab m10 step 6): Delete the stack and confirm that the resources created by the stack are removed.

## Verify

### Lab m10

- [ ] **V-m10.1** (checks DoD-m10.1): Check Parameters, Resources and Outputs are identified in the short YAML template. *Validates R-10.1, B-m10.1.*
- [ ] **V-m10.2** (checks DoD-m10.2): Check the logical ID and type of the sample bucket resource are identified. *Validates R-10.2, B-m10.2.*
- [ ] **V-m10.3** (checks DoD-m10.3): Check the starter stack is deployed and its status and events are reviewed. *Validates R-10.3, R-10.4, B-m10.3, B-m10.4.*
- [ ] **V-m10.4** (checks DoD-m10.4): Check the parameter or tag change is applied as a stack update and the result is observed. *Validates R-10.3, B-m10.5.*
- [ ] **V-m10.5** (checks DoD-m10.5): Check the stack is deleted and the resources it created are confirmed removed. *Validates R-10.3, B-m10.6.*
