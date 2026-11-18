# m06: Networking Fundamentals

**Schedule:** Day 7 · **Builds on:** `05-m05-cp2-static-website-gallery` · **Feeds into:** `07-m07-compute-fundamentals` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee describes how an instance receives network connectivity in a VPC and names the first place to look when a connection fails, after inspecting a prepared VPC, subnet, route table and Security Group.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 6.1 | VPCs, CIDR ranges and subnets | 1.0 h | VPC, CIDR range, private network boundary, Availability Zone, subnet | What does a VPC's CIDR range decide, and how is a subnet related to an Availability Zone? | Steps 1–2: Find the CIDR range, a subnet and its Availability Zone |
| 6.2 | Public subnets, route tables and Internet Gateways | 1.0 h | public subnet, route table, default route, Internet Gateway, attachment to a VPC | What makes a subnet public rather than private, and what does the trainee check first when an instance in it cannot be reached? | Step 3 and the optional row: Find the route to the Internet Gateway |
| 6.3 | Security Groups, NACLs and out-of-scope concepts | 1.25 h | Security Group, stateful firewall, inbound rule, network ACL, private subnet, NAT Gateway, VPC endpoint (concepts only) | How do a Security Group and a network ACL differ in where they apply and in how they treat return traffic? | Step 4: Find an inbound HTTP rule |
| | **Total** | **3.25 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Tools | The VPC Console. |
| Provided material | A prepared VPC with at least one subnet, a route table with a route to an Internet Gateway, and a Security Group with an inbound HTTP rule. |
| Scope control | Not required: NAT Gateways, multiple private subnets, VPC peering, Transit Gateway, VPN, or complex network ACL designs. Private subnets, NAT Gateway and VPC endpoints are concepts only. |
| Creation exercise | Creating a simple VPC with one public subnet and an Internet Gateway is optional and happens only if the sandbox permissions allow. |
| Reference reading | The study material for this self-paced stage: [What is Amazon VPC?](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html), [Subnet route tables](https://docs.aws.amazon.com/vpc/latest/userguide/subnet-route-tables.html), [Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-security-groups.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m06: Inspect a prepared network

| Step | What the trainee does |
| --- | --- |
| 1 | Inspects a prepared VPC and identifies its CIDR range. |
| 2 | Identifies one subnet and the Availability Zone in which it resides. |
| 3 | Inspects the route table and locates the route to the Internet Gateway. |
| 4 | Inspects a Security Group and identifies an inbound HTTP rule. |
| Optional | Creates a simple VPC with one public subnet and an Internet Gateway, if the sandbox permissions allow. |
| **Acceptance** | The CIDR range of the prepared VPC is identified. A subnet and the Availability Zone it resides in are identified. The route to the Internet Gateway is located in the route table. An inbound HTTP rule is identified in a Security Group. The trainee describes how an instance receives network connectivity. The trainee names the first place to look when a connection fails. |

## Deliverable

The deliverable contains:

- [ ] Screenshot of the VPC with its CIDR range
- [ ] Screenshot of a subnet with its Availability Zone
- [ ] Screenshot of the route table with the Internet Gateway route
- [ ] Screenshot of the Security Group's inbound HTTP rule
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which prepared VPC, subnet and Security Group are used? | Every lab chunk inspects them |
| Do the sandbox permissions allow creating a VPC? | The optional row depends on it |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
