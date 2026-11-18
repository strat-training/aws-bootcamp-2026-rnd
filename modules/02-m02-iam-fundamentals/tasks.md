# m02: IAM Fundamentals: Tasks

**Objective:** The trainee explains who or what is making an AWS request, what permission it needs, and how a role's trust policy differs from its permissions policy, using a pre-created training role, a sample policy and a policy test, without creating any permanent IAM user or long-term access key.

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
| 2.1 Identities: users, groups and roles | R-2.1 | B-m02.1 | V-m02.1, V-m02.6 (DoD-m02.1, DoD-m02.6) |
| 2.2 Policies: Allow, Deny and policy types | R-2.2 | B-m02.2, B-m02.3 | V-m02.2, V-m02.3 (DoD-m02.2, DoD-m02.3) |
| 2.3 Trust, permissions and AWS STS | R-2.3 | B-m02.4, B-m02.O1 | V-m02.4, V-m02.5 (DoD-m02.4, DoD-m02.5) |

## Research

- [ ] **R-2.1** (Scope 2.1): Answer in writing: why should the sandbox rely on roles and temporary credentials instead of shared long-term access keys, and what does least privilege change about who can do what? Look in the IAM documentation on security best practices.
- [ ] **R-2.2** (Scope 2.2): Answer in writing: how do you decide from a policy whether a request is allowed or denied, and when is a resource-based policy used instead of an identity-based one? Look in the IAM documentation on policies and on testing policies.
- [ ] **R-2.3** (Scope 2.3): Answer in writing: what is the difference between who may assume a role and what the assumed role may do, and why does the difference matter when a request is denied? Look in the IAM documentation on roles and in the AWS STS documentation.

## Build

### Lab m02: Read policies and separate trust from permissions

- [ ] **B-m02.1** (Lab m02 step 1): Inspect a pre-created training role and review its attached permissions.
- [ ] **B-m02.2** (Lab m02 step 2): Open a sample policy and identify its Effect, Action and Resource.
- [ ] **B-m02.3** (Lab m02 step 3): Use the IAM Policy Simulator, or an instructor-provided example, to test one allowed and one denied request.
- [ ] **B-m02.4** (Lab m02 step 4): Review the starter trust policy and identify the trusted principal.
- [ ] **B-m02.O1** (Lab m02 optional row, optional): Walk through a simple role-assumption flow inside the training environment, if the instructor has enabled it.

## Verify

### Lab m02

- [ ] **V-m02.1** (checks DoD-m02.1): Check the permissions attached to the training role are listed. *Validates R-2.1, B-m02.1.*
- [ ] **V-m02.2** (checks DoD-m02.2): Check Effect, Action and Resource are identified in the sample policy. *Validates R-2.2, B-m02.2.*
- [ ] **V-m02.3** (checks DoD-m02.3): Check one allowed and one denied request are shown with the policy test. *Validates R-2.2, B-m02.3.*
- [ ] **V-m02.4** (checks DoD-m02.4): Check the trusted principal in the starter trust policy is identified. *Validates R-2.3, B-m02.4.*
- [ ] **V-m02.5** (checks DoD-m02.5): Check there is a written explanation, in your own words, of the difference between trust and permissions. *Validates R-2.3, B-m02.1, B-m02.4.*
- [ ] **V-m02.6** (checks DoD-m02.6): Check no IAM user or long-term access key was created for this stage. *Validates R-2.1, B-m02.1, B-m02.2, B-m02.3, B-m02.4.*
