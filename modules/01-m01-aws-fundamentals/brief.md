# m01: AWS Fundamentals

**Schedule:** Day 2 · **Builds on:** none (course entry point) · **Feeds into:** `02-m02-iam-fundamentals` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee navigates the AWS Console in the assigned sandbox, identifies the active account, Region and identity from the Console and from a CLI identity check, and explains why those three are checked before any resource is created.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 1.1 | Cloud computing and the AWS global footprint | 1.75 h | cloud computing, common AWS use cases, IaaS, PaaS, SaaS, Region, Availability Zone, Edge Location | Why can a resource created in one Region be missing from the view of another, and what does that change about what the trainee checks before creating anything? | Step 4: Observe Region-specific views |
| 1.2 | Accounts and the Shared Responsibility Model | 1.25 h | AWS account, account boundary, resource organization, Shared Responsibility Model | Where does AWS's responsibility end and the trainee's begin for a resource created in a sandbox account, and why does the account boundary matter? | Step 3: Identify the account ID and ARN |
| 1.3 | Console, CloudShell and the AWS CLI | 2.0 h | AWS Management Console, AWS CloudShell, AWS CLI, `aws sts get-caller-identity`, account ID, ARN, active identity, IAM Identity Center sign-in | How does the trainee confirm which account, Region and identity a command will act on before creating anything, and why must long-term access keys not be created or shared? | Steps 1–2: Sign in and run the identity check |
| 1.4 | Pricing, budgets, tags and cleanup | 1.75 h | pricing fundamentals, budgets, cost monitoring, tags, resource cleanup | Which habits stop a sandbox from accumulating cost, and where does the trainee look to see spend? | Step 5: Locate budget or cost information |
| | **Total** | **6.75 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Prerequisite knowledge | Basic computer literacy and the ability to navigate a browser and file system. No prior AWS experience is assumed. Basic command-line familiarity helps, because AWS CLI usage is introduced here. |
| Tools | AWS Management Console, AWS CloudShell and a text editor such as VS Code. A local AWS CLI installation is optional when CloudShell is used. |
| Environment | The instructor-provided Sandbox 3 and Sandbox 4 only, never personal or production accounts. One Region throughout the bootcamp, named in the header. All work stays within the sandbox permissions. |
| Authentication | The approved sandbox sign-in method. Root credentials are not used or shared, and no long-term access keys are created or shared. |
| Data | Non-sensitive training content only. |
| Cost control | Small approved resource sizes only. Public IPv4 addresses, running compute, data transfer, requests and log storage can incur charges, and pricing varies by Region. |
| Cleanup | Resources that are no longer needed are removed at the end of each lab. S3 buckets are emptied before they are deleted. |
| Troubleshooting order | Confirm the account and Region. Confirm the identity and permissions. Confirm the resource name and configuration. Check the network path and Security Group when connectivity is involved. Review service status, metrics, logs or stack events. Change one thing at a time and retest. Record the symptom, the cause and the fix. |
| Assessment | Only the three checkpoints (`cp1`, `cp2`, `cp3`) are graded, and a trainee must pass all three, with a focused retry allowed after feedback. Module labs are practice, checked against their Acceptance rows. |
| Reference reading | The study material for this self-paced stage: [AWS CLI with IAM Identity Center](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sso.html), [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/), [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html), [AWS Pricing Calculator](https://calculator.aws/), [EC2 pricing](https://aws.amazon.com/ec2/pricing/on-demand/). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m01: Confirm the account, Region and identity

| Step | What the trainee does |
| --- | --- |
| 1 | Signs in to the assigned sandbox and locates the account and Region shown in the Console. |
| 2 | Opens AWS CloudShell and runs `aws sts get-caller-identity`. |
| 3 | Identifies the account ID and ARN in the command output. |
| 4 | Changes the Console Region, observes that resource views are Region-specific, and switches back to Singapore. |
| 5 | Reviews where the account budget or cost monitoring information is displayed. |
| **Acceptance** | The account ID and ARN from the identity check match the assigned sandbox. The trainee names the Region shown in the Console and shows that resource views change when the Region changes. The trainee points to where budget or cost monitoring information is displayed. The trainee explains why the account, Region and identity are checked before creating resources. |

## Deliverable

The deliverable contains:

- [ ] Screenshot of the Console showing the account and Region
- [ ] The identity-check output, redacted as needed
- [ ] Screenshots of the same Console view in two Regions
- [ ] Screenshot of where budget or cost information is displayed
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which sign-in method applies to the sandbox? | Lab chunk 1.3 depends on it |
| Which budget or cost view is available to trainees in the sandbox? | Lab chunk 1.4 depends on what the sandbox permissions show |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
