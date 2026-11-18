# m07: Compute Fundamentals

**Schedule:** Day 7 · **Builds on:** `06-m06-networking-fundamentals` · **Feeds into:** `08-m08-monitoring-and-operations` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee launches a small EC2 instance into a public subnet, permits HTTP for the lab, starts a simple web server with a User Data script, reaches the page from a browser, and identifies the AMI, instance type, subnet, public address and Security Group of the instance.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 7.1 | EC2 instances, AMIs and instance types | 1.0 h | EC2 instance, common use cases, AMI, instance type, instance lifecycle (pending, running, stopping, terminated), EBS volume | What does the trainee weigh when picking an AMI and an instance type for a small training web server, and what happens to the instance and its disk at each lifecycle state? | Steps 1–2, 6 and 7: Choose, launch, review and terminate |
| 7.2 | Instance networking and web access | 1.25 h | public subnet, public address, Security Group inbound and outbound rules, HTTP, status checks | Why is HTTP opened for the lab while SSH is not opened to the entire internet, and what does the trainee check first when the page does not load? | Steps 3 and 5: Permit HTTP and test the page |
| 7.3 | User Data and managed access | 1.25 h | User Data, first-boot configuration, IAM role for EC2, AWS Systems Manager Session Manager | Why is managed access preferred to opening SSH, and why does an EC2 IAM role remove the need for access keys on the instance? | Step 4 and the optional row: Start the web server and observe managed access |
| | **Total** | **3.5 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Provided material | An instructor-approved AMI and small instance type, the instructor-prepared public subnet or the approved default VPC, and a short instructor-provided User Data script. |
| Network exposure | HTTP is opened for the lab. SSH is never opened to the entire internet. |
| Cost control | One small instance. A public IPv4 address and running compute can incur charges. |
| Cleanup | The instance is terminated after testing unless the instructor has designated it for reuse. |
| Reference reading | The study material for this self-paced stage: [Get started with Amazon EC2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html), [EC2 User Data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m07: Launch an instance and serve a web page

| Step | What the trainee does |
| --- | --- |
| 1 | Selects an instructor-approved AMI and a small instance type. |
| 2 | Launches an instance into the instructor-prepared public subnet or the approved default VPC. |
| 3 | Configures a Security Group that permits HTTP for the lab, without opening SSH to the entire internet. |
| 4 | Uses a short instructor-provided User Data script to install and start a web server. |
| 5 | Waits for the instance status checks and tests the HTTP page using the public address. |
| 6 | Reviews the instance details, status checks and basic monitoring information. |
| 7 | Terminates the instance after testing, unless the instructor has designated it for reuse. |
| Optional | Before step 7, if the approved setup attaches an IAM role to the instance, observes how the role grants AWS service permissions without storing access keys on the instance. |
| **Acceptance** | The instance uses the instructor-approved AMI and a small instance type, in the prepared public subnet or the approved default VPC. The Security Group permits HTTP for the lab, and SSH is not open to the entire internet. The instance passes its status checks. The web page is reachable from a browser using the public address. The trainee identifies the AMI, instance type, subnet, public address and Security Group. The instance is terminated after testing, unless the instructor designated it for reuse. |

## Deliverable

The deliverable contains:

- [ ] Screenshot of the instance details showing the AMI, instance type, subnet, public address and Security Group
- [ ] Screenshot of the Security Group's inbound rules
- [ ] Browser screenshot of the web page with the URL used
- [ ] Evidence that the instance was terminated, or a note that the instructor designated it for reuse
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which AMI, instance type and subnet or default VPC are approved? | Lab chunks 7.1 and 7.2 |
| Which User Data script is provided? | Lab chunk 7.3 |
| Is the instance designated for reuse in m08? | Step 7 and the metrics review in m08 |
| Does the approved setup attach an IAM role to the lab instance? | The optional row depends on it |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
