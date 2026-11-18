# m02: IAM Fundamentals

**Schedule:** Day 3 · **Builds on:** `01-m01-aws-fundamentals` · **Feeds into:** `03-m03-cp1-cross-account-iam` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee explains who or what is making an AWS request, what permission it needs, and how a role's trust policy differs from its permissions policy, using a pre-created training role, a sample policy and a policy test, without creating any permanent IAM user or long-term access key.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 2.1 | Identities: users, groups and roles | 1.5 h | IAM user, IAM group, IAM role, principal, least privilege, long-term access key, temporary credentials | Why should the sandbox rely on roles and temporary credentials instead of shared long-term access keys, and what does least privilege change about who can do what? | Step 1: Inspect the training role |
| 2.2 | Policies: Allow, Deny and policy types | 2.25 h | policy document, Effect, Action, Resource, Allow, Deny, identity-based policy, resource-based policy, IAM Policy Simulator | How does the trainee decide from a policy whether a request is allowed or denied, and when is a resource-based policy used instead of an identity-based one? | Steps 2–3: Read a policy and test it |
| 2.3 | Trust, permissions and AWS STS | 3.0 h | trust policy, permissions policy, trusted principal, AWS STS, role assumption, temporary credentials | What is the difference between who may assume a role and what the assumed role may do, and why does the difference matter when a request is denied? | Step 4 and the optional row: Trust policy and role assumption |
| | **Total** | **6.75 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Tools | The IAM Console and the IAM Policy Simulator, or an instructor-provided example if the simulator is not available. |
| Provided material | A pre-created training role, a sample policy and a starter trust policy from the instructor. |
| Access method | The sandbox access method provided by the instructor. The trainee does not create permanent IAM users or generate long-term access keys. |
| Scope | Beginner level. Role assumption is walked through only if the training environment enables it. |
| Reference reading | The study material for this self-paced stage: [IAM Security Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html), [IAM Policy Simulator](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_testing-policies.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m02: Read policies and separate trust from permissions

| Step | What the trainee does |
| --- | --- |
| 1 | Inspects a pre-created training role and reviews its attached permissions. |
| 2 | Opens a sample policy and identifies its Effect, Action and Resource. |
| 3 | Uses the IAM Policy Simulator, or an instructor-provided example, to test one allowed and one denied request. |
| 4 | Reviews the starter trust policy and identifies the trusted principal. |
| Optional | Walks through a simple role-assumption flow inside the training environment, if the instructor has enabled it. |
| **Acceptance** | The permissions attached to the training role are listed. Effect, Action and Resource are identified in the sample policy. One allowed and one denied request are shown with the policy test. The trusted principal in the starter trust policy is identified. The trainee explains the difference between trust (who may assume a role) and permissions (what the assumed role may do). No IAM user or long-term access key was created for this stage. |

## Deliverable

The deliverable contains:

- [ ] The training role's attached permissions, as a screenshot or notes
- [ ] The sample policy with its Effect, Action and Resource annotated
- [ ] The policy-test output showing one allowed and one denied request
- [ ] The starter trust policy with the trusted principal annotated
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which training role, sample policy and starter trust policy are provided? | Lab chunks 2.1, 2.2 and 2.3 are all built on them |
| Is role assumption enabled in the training environment? | The optional row depends on it |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
