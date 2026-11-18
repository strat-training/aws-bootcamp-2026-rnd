# m06: Networking Fundamentals: Tasks

**Objective:** The trainee describes how an instance receives network connectivity in a VPC and names the first place to look when a connection fails, after inspecting a prepared VPC, subnet, route table and Security Group.

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
| 6.1 VPCs, CIDR ranges and subnets | R-6.1 | B-m06.1, B-m06.2 | V-m06.1, V-m06.2, V-m06.5 (DoD-m06.1, DoD-m06.2, DoD-m06.5) |
| 6.2 Public subnets, route tables and Internet Gateways | R-6.2 | B-m06.3, B-m06.O1 | V-m06.3, V-m06.6 (DoD-m06.3, DoD-m06.6) |
| 6.3 Security Groups, NACLs and out-of-scope concepts | R-6.3 | B-m06.4 | V-m06.4 (DoD-m06.4) |

## Research

- [ ] **R-6.1** (Scope 6.1): Answer in writing: what does a VPC's CIDR range decide, and how is a subnet related to an Availability Zone? Look in the Amazon VPC documentation on VPCs and subnets.
- [ ] **R-6.2** (Scope 6.2): Answer in writing: what makes a subnet public rather than private, and what is the first thing to check when an instance in it cannot be reached? Look in the Amazon VPC documentation on subnet route tables and Internet gateways.
- [ ] **R-6.3** (Scope 6.3): Answer in writing: how do a Security Group and a network ACL differ in where they apply and in how they treat return traffic? Look in the Amazon VPC documentation on Security Groups and network ACLs.

## Build

### Lab m06: Inspect a prepared network

- [ ] **B-m06.1** (Lab m06 step 1): Inspect the prepared VPC and identify its CIDR range.
- [ ] **B-m06.2** (Lab m06 step 2): Identify one subnet and the Availability Zone in which it resides.
- [ ] **B-m06.3** (Lab m06 step 3): Inspect the route table and locate the route to the Internet Gateway.
- [ ] **B-m06.4** (Lab m06 step 4): Inspect a Security Group and identify an inbound HTTP rule.
- [ ] **B-m06.O1** (Lab m06 optional row, optional): Create a simple VPC with one public subnet and an Internet Gateway, if the sandbox permissions allow.

## Verify

### Lab m06

- [ ] **V-m06.1** (checks DoD-m06.1): Check the CIDR range of the prepared VPC is identified. *Validates R-6.1, B-m06.1.*
- [ ] **V-m06.2** (checks DoD-m06.2): Check a subnet and the Availability Zone it resides in are identified. *Validates R-6.1, B-m06.2.*
- [ ] **V-m06.3** (checks DoD-m06.3): Check the route to the Internet Gateway is located in the route table. *Validates R-6.2, B-m06.3.*
- [ ] **V-m06.4** (checks DoD-m06.4): Check an inbound HTTP rule is identified in a Security Group. *Validates R-6.3, B-m06.4.*
- [ ] **V-m06.5** (checks DoD-m06.5): Check there is a description of how an instance receives network connectivity. *Validates R-6.1, R-6.2, R-6.3, B-m06.1, B-m06.2, B-m06.3, B-m06.4.*
- [ ] **V-m06.6** (checks DoD-m06.6): Check there is a named first place to look when a connection fails. *Validates R-6.2, B-m06.3, B-m06.4.*
