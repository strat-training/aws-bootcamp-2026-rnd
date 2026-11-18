# m03: Cross-Account IAM Access: Tasks

**Objective:** None yet. The brief has no objective for this stage (it is marked TODO for the trainer).

> **Pending: this file holds research tasks only.** The Build and Verify sections are pending: the trainer has not yet supplied the lab or the definition of done in [`m03-brief.md`](m03-brief.md), so there are no lab steps or Acceptance clauses to plan from, and none were invented. Once they exist, regenerate this file with `/trainee-task-planner re-plan modules/03-m03-cp1-cross-account-iam m03`.

> There is no solutions file for this stage. This checklist guides the work, it does not contain it. Source of every task: [`m03-brief.md`](m03-brief.md).

> **Region:** do all of this in Asia Pacific (Singapore), `ap-southeast-1`.

## ID scheme

| Prefix | Meaning | Source in the brief |
| --- | --- | --- |
| `R-<subject>` | Research task | One per row of the Scope table |
| `B-<lab>.<step>` | Build task | Pending: the brief has no lab yet |
| `V-<lab>.<n>` | Verify task, checks `DoD-<lab>.<n>` | Pending: the brief has no definition of done yet |

## Traceability

| Subject | Research | Build | Verify (DoD) |
| --- | --- | --- | --- |
| 3.1 Cross-account access architecture | R-3.1 | pending | pending |
| 3.2 Role trust and AssumeRole | R-3.2 | pending | pending |
| 3.3 Cross-account S3 access and AccessDenied troubleshooting | R-3.3 | pending | pending |

## Research

- [ ] **R-3.1** (Scope 3.1): Answer in writing: why does the platform team use a role in the destination account instead of creating permanent users there? Look in the AWS IAM documentation on roles and temporary credentials.
- [ ] **R-3.2** (Scope 3.2): Answer in writing: which permissions must exist, and in which accounts, before a source identity can assume a destination role? Look in the AWS IAM documentation on cross-account access with roles.
- [ ] **R-3.3** (Scope 3.3): Answer in writing: when a role-assumption call or an S3 request returns AccessDenied, which checks come first, and in what order? Look in the AWS documentation on troubleshooting access-denied errors.

## Build

Pending. The brief has no lab for this stage yet.

## Verify

Pending. The brief has no definition of done for this stage yet.
