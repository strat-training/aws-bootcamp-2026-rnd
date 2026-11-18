# m07: Compute Fundamentals: Tasks

**Objective:** The trainee launches a small EC2 instance into a public subnet, permits HTTP for the lab, starts a simple web server with a User Data script, reaches the page from a browser, and identifies the AMI, instance type, subnet, public address and Security Group of the instance.

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
| 7.1 EC2 instances, AMIs and instance types | R-7.1 | B-m07.1, B-m07.2, B-m07.6, B-m07.7 | V-m07.1, V-m07.5, V-m07.6 (DoD-m07.1, DoD-m07.5, DoD-m07.6) |
| 7.2 Instance networking and web access | R-7.2 | B-m07.3, B-m07.5 | V-m07.2, V-m07.3, V-m07.4 (DoD-m07.2, DoD-m07.3, DoD-m07.4) |
| 7.3 User Data and managed access | R-7.3 | B-m07.4, B-m07.O1 | V-m07.2, V-m07.4 (DoD-m07.2, DoD-m07.4) |

## Research

- [ ] **R-7.1** (Scope 7.1): Answer in writing: what do you weigh when picking an AMI and an instance type for a small training web server, and what happens to the instance and its disk at each lifecycle state? Look in the EC2 documentation on AMIs, instance types, the instance lifecycle and EBS volumes.
- [ ] **R-7.2** (Scope 7.2): Answer in writing: why is HTTP opened for the lab while SSH is not opened to the entire internet, and what do you check first when the page does not load? Look in the VPC documentation on Security Groups and in the EC2 documentation on status checks.
- [ ] **R-7.3** (Scope 7.3): Answer in writing: why is managed access preferred to opening SSH, and why does an EC2 IAM role remove the need for access keys on the instance? Look in the EC2 documentation on IAM roles for instances and in the Systems Manager documentation on Session Manager.

## Build

### Lab m07: Launch an instance and serve a web page

- [ ] **B-m07.1** (Lab m07 step 1): Select an instructor-approved AMI and a small instance type.
- [ ] **B-m07.2** (Lab m07 step 2): Launch an instance into the instructor-prepared public subnet or the approved default VPC.
- [ ] **B-m07.3** (Lab m07 step 3): Configure a Security Group that permits HTTP for the lab, without opening SSH to the entire internet.
- [ ] **B-m07.4** (Lab m07 step 4): Use the short instructor-provided User Data script to install and start a web server.
- [ ] **B-m07.5** (Lab m07 step 5): Wait for the instance status checks and test the HTTP page using the public address.
- [ ] **B-m07.6** (Lab m07 step 6): Review the instance details, status checks and basic monitoring information.
- [ ] **B-m07.7** (Lab m07 step 7): Terminate the instance after testing, unless the instructor has designated it for reuse.
- [ ] **B-m07.O1** (Lab m07 optional row, optional): Before step 7, if the approved setup attaches an IAM role to the instance, observe how the role grants AWS service permissions without storing access keys on the instance.

## Verify

### Lab m07

- [ ] **V-m07.1** (checks DoD-m07.1): Check the instance uses the instructor-approved AMI and a small instance type, in the prepared public subnet or the approved default VPC. *Validates R-7.1, B-m07.1, B-m07.2.*
- [ ] **V-m07.2** (checks DoD-m07.2): Check the Security Group permits HTTP for the lab, and SSH is not open to the entire internet. *Validates R-7.2, R-7.3, B-m07.3.*
- [ ] **V-m07.3** (checks DoD-m07.3): Check the instance passes its status checks. *Validates B-m07.5, B-m07.6.*
- [ ] **V-m07.4** (checks DoD-m07.4): Check the web page is reachable from a browser using the public address. *Validates R-7.2, B-m07.4, B-m07.5.*
- [ ] **V-m07.5** (checks DoD-m07.5): Check the AMI, instance type, subnet, public address and Security Group of the instance are each identified. *Validates R-7.1, B-m07.1, B-m07.2, B-m07.3, B-m07.6.*
- [ ] **V-m07.6** (checks DoD-m07.6): Check the instance is terminated after testing, unless the instructor designated it for reuse. *Validates R-7.1, B-m07.7.*
