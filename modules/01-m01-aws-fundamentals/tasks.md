# m01: AWS Fundamentals: Tasks

**Objective:** The trainee navigates the AWS Console in the assigned sandbox, identifies the active account, Region and identity from the Console and from a CLI identity check, and explains why those three are checked before any resource is created.

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
| 1.1 Cloud computing and the AWS global footprint | R-1.1 | B-m01.4 | V-m01.2 (DoD-m01.2) |
| 1.2 Accounts and the Shared Responsibility Model | R-1.2 | B-m01.3 | V-m01.1 (DoD-m01.1) |
| 1.3 Console, CloudShell and the AWS CLI | R-1.3 | B-m01.1, B-m01.2 | V-m01.1, V-m01.4 (DoD-m01.1, DoD-m01.4) |
| 1.4 Pricing, budgets, tags and cleanup | R-1.4 | B-m01.5 | V-m01.3 (DoD-m01.3) |

## Research

- [ ] **R-1.1** (Scope 1.1): Answer in writing: why can a resource created in one Region be missing from the view of another, and what does that change about what to check before creating anything? Look in the AWS documentation on Regions and Availability Zones.
- [ ] **R-1.2** (Scope 1.2): Answer in writing: where does AWS's responsibility end and yours begin for a resource created in a sandbox account, and why does the account boundary matter? Look in the AWS Shared Responsibility Model documentation.
- [ ] **R-1.3** (Scope 1.3): Answer in writing: how do you confirm which account, Region and identity a command will act on before creating anything, and why must long-term access keys not be created or shared? Look in the AWS CLI and IAM Identity Center sign-in documentation.
- [ ] **R-1.4** (Scope 1.4): Answer in writing: which habits stop a sandbox from accumulating cost, and where do you look to see spend? Look in the AWS pricing and AWS Budgets documentation.

## Build

### Lab m01: Confirm the account, Region and identity

- [ ] **B-m01.1** (Lab m01 step 1): Sign in to the assigned sandbox and locate the account and Region shown in the Console.
- [ ] **B-m01.2** (Lab m01 step 2): Open AWS CloudShell and run `aws sts get-caller-identity`.
- [ ] **B-m01.3** (Lab m01 step 3): Identify the account ID and ARN in the command output.
- [ ] **B-m01.4** (Lab m01 step 4): Change the Console Region, observe that resource views are Region-specific, and switch back to Singapore.
- [ ] **B-m01.5** (Lab m01 step 5): Review where the account budget or cost monitoring information is displayed.

## Verify

### Lab m01

- [ ] **V-m01.1** (checks DoD-m01.1): Check the account ID and ARN from the identity check match the assigned sandbox. *Validates R-1.2, R-1.3, B-m01.2, B-m01.3.*
- [ ] **V-m01.2** (checks DoD-m01.2): Check the Region shown in the Console is named, and that resource views change when the Region changes. *Validates R-1.1, B-m01.1, B-m01.4.*
- [ ] **V-m01.3** (checks DoD-m01.3): Check where budget or cost monitoring information is displayed can be pointed to. *Validates R-1.4, B-m01.5.*
- [ ] **V-m01.4** (checks DoD-m01.4): Check there is an explanation of why the account, Region and identity are checked before creating resources. *Validates R-1.1, R-1.3, B-m01.1, B-m01.2, B-m01.3, B-m01.4.*
