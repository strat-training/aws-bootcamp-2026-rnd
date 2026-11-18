# m03: Cross-Account IAM Access

**Schedule:** Day 4 (study part) · **Builds on:** `02-m02-iam-fundamentals` · **Feeds into:** [`cp1-brief.md`](cp1-brief.md), the activity in this folder · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

> **DRAFT for trainer review. Nothing here is approved.** The source gives this module only a one-line focus (*cross-account access architecture, IAM role trust relationships, AssumeRole, temporary credentials, cross-account S3 access, and AccessDenied troubleshooting*). The Objective, Lab, Acceptance row and Deliverable below are drafted from the source's program outcomes, its Day 4 plan, its reference reading and Activity 1 (`cp1`). The course is self-paced, so there is no instructor demonstration. The sources and the judgements to confirm are in the review notes at the end. Delete this banner and those notes once approved.

## Objective

By the end of this stage, the trainee traces how a source identity in one AWS account assumes a role in another account to reach one approved S3 bucket, explains which policy controls the trust relationship and which controls the S3 permissions, and lists the first checks when access is denied, ready to configure it in `cp1`.

## Scope

The hours are drafts: the source's generic daily plan sets aside 120 minutes for concepts and demonstration ahead of the activity block, which `cp1` takes. With no instructor demonstration, that time is self-study of the reference reading. The Research questions are drafts.

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 3.1 | Cross-account access architecture | 0.75 h | cross-account access, source account, destination account, source identity, destination role, temporary credentials | Why does the platform team use a role in the destination account instead of creating permanent users there? | Step 1: Name each element of the flow |
| 3.2 | Role trust and AssumeRole | 0.75 h | IAM role trust relationship, trust policy, `sts:AssumeRole`, trusted principal, temporary credentials | Which permissions must exist, and in which accounts, before a source identity can assume a destination role? | Steps 2–3: Read the starter policies and the tutorial |
| 3.3 | Cross-account S3 access and AccessDenied troubleshooting | 0.5 h | cross-account S3 access, permissions policy, scoped access, AccessDenied, first checks | When an AssumeRole call or an S3 request returns AccessDenied, which checks come first, and in what order? | Step 4: Map the first checks to where they are made |
| | **Total** | **2.0 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Accounts | Sandbox 3 and Sandbox 4 are the two distinct accounts. The recommended mapping is Sandbox 3 as the source and Sandbox 4 as the destination, unless the sandbox administrator provisioned the reverse. |
| Credentials | Only temporary credentials. No permanent users are created in the destination account, and no long-term access keys are created or shared. |
| Provided material | The reference architecture figure and the starter trust-policy and permissions-policy examples that `cp1` uses, and the beginner troubleshooting guide. |
| Scope | Study only. No resources are created in this stage, and the hands-on build is `cp1`. |
| Reference reading | The study material for this self-paced stage. The primary guide is the [Tutorial: Delegate access across AWS accounts using IAM roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_cross-account-with-roles.html). Optional pre-reading: [Cross-Account Access Explained](https://medium.com/@varun.thantry07/aws-cross-account-access-explained-securely-share-resources-across-aws-accounts-c254c93993c5). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m03: Trace a cross-account role assumption

| Step | What the trainee does |
| --- | --- |
| 1 | Studies the reference architecture figure and names each element of the flow and the account it sits in: the source identity, the role assumption and the temporary credentials, the destination role with its trust policy and limited permissions, the source-side permission, and the approved S3 bucket. |
| 2 | Opens the starter trust-policy and permissions-policy examples that `cp1` uses, and identifies the trusted principal in the trust policy, the actions and the resource in the permissions policy, and what each placeholder (account ID, role ARN, bucket name) stands for. |
| 3 | Reads the AWS tutorial on delegating access across accounts with IAM roles, which is the primary implementation guide for `cp1`, and records, for each configuration step in it, which account and which policy it belongs to. |
| 4 | Takes the first checks that the beginner troubleshooting guide lists for an AssumeRole AccessDenied and for a denied S3 upload or download, and notes for each check where it is made: which account, and which policy or setting. |
| Optional | Reads the supplementary cross-account access article that the source offers as optional pre-reading. |
| **Acceptance** | Each element of the reference architecture is named, with the account it sits in. The trusted principal and the placeholders are identified in both starter policies. The trainee explains which policy controls the trust relationship and which controls the S3 permissions. The trainee describes how the source identity receives temporary credentials for the destination role. The first checks for an AssumeRole AccessDenied and for a denied S3 request are listed, each with where it is made. The trainee states why the destination account uses a role instead of permanent users. |

## Deliverable

The deliverable contains:

- [ ] The reference architecture with each element named and its account marked
- [ ] The starter trust-policy and permissions-policy examples, annotated with the trusted principal, the actions, the resource and the placeholders
- [ ] Notes from the tutorial: each configuration step with its account and policy
- [ ] The first checks for an AssumeRole AccessDenied and for a denied S3 request, each with where it is made
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which reference architecture figure and starter policy examples are handed out in this stage? | Steps 1 and 2, and `cp1` uses the same files |
| Is Sandbox 3 the source and Sandbox 4 the destination, or the reverse? | The Accounts constraint, and `cp1` |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |

## Draft review notes (delete once approved)

| Item | Where it comes from | Judgement to confirm |
| --- | --- | --- |
| Objective | The focus line, and the program outcomes *describe IAM users, roles, policies, trust relationships, and least-privilege access* and *use Sandbox 3 and Sandbox 4 for a guided cross-account role-assumption exercise and verify an allowed and denied action* | It stops at "ready to configure it in `cp1`", because the source puts the build in Activity 1 |
| Lab shape | The Day 4 plan gives the guided-lab block to the Activity and leaves this module only concepts and demonstration time. With no demonstration, the lab is built from the figure, the starter files, the tutorial and the troubleshooting guide | The lab creates no cloud resources, so there is nothing to clean up. The alternative is no lab and a flat `DoD-01`, `DoD-02`, ... list |
| Step 1 | Figure 1 and its caption in Activity 1 | |
| Step 2 | The instructor-provided starter policies in Activity 1 | It reads `cp1`'s own starter files without filling them in. Drop it if `cp1` should be the first contact with them |
| Step 3 | The source names the AWS cross-account tutorial as the primary implementation guide for Activity 1 | It replaces the instructor demonstration of the first draft. The tutorial may expect a hands-on run, so this step is reading only |
| Step 4 | The "AssumeRole returns AccessDenied" and "S3 upload or download is denied" rows of the beginner troubleshooting guide | |
| Optional row | The source's supplementary article, offered as optional pre-reading for Activity 1 | |
| Acceptance | Clauses 3 and 4 come from Activity 1's "basic explanation" pass condition and learner step 8. Clause 6 comes from its business scenario | Clauses 1, 2 and 5 restate what steps 1, 2 and 4 produce, because the source gives no module-level expected output. `DoD-cp1.5` asks for a similar explanation, which is intended as rehearsal |
