# Checkpoint 1: The Account Access Challenge: Tasks

**Objective:** Set up a role in Account B that the approved identity in Account A can assume, then use it to reach only the approved bucket.

> There is no solutions file for this checkpoint. This checklist guides the work, it does not contain it. Source of every task: [`cp1-brief.md`](cp1-brief.md). A checkpoint brief has no Scope table and no Research column, so there are no research tasks. Its diagram and hand-in items are listed in section 5 of the brief and are not tasks.

> **Region:** do all of this in Asia Pacific (Singapore), `ap-southeast-1`.

## ID scheme

| Prefix | Meaning | Source in the brief |
| --- | --- | --- |
| `B-cp1.<step>` | Build task | One per row of the Your Steps table (section 3) |
| `V-cp1.<n>` | Verify task, checks `DoD-cp1.<n>` | The n-th row of the How You'll Know You're Done table (section 4) |

## Traceability

| Step | Build | Verify (DoD) |
| --- | --- | --- |
| 1. Get ready | B-cp1.1 | V-cp1.5 (DoD-cp1.5) |
| 2. Build it | B-cp1.2 | V-cp1.1, V-cp1.2, V-cp1.3 (DoD-cp1.1, DoD-cp1.2, DoD-cp1.3) |
| 3. Try it out | B-cp1.3 | V-cp1.3, V-cp1.4, V-cp1.6 (DoD-cp1.3, DoD-cp1.4, DoD-cp1.6) |
| 4. Fix what's broken | B-cp1.4 | V-cp1.4 (DoD-cp1.4) |
| 5. Wrap up | B-cp1.5 | V-cp1.5, V-cp1.6 (DoD-cp1.5, DoD-cp1.6) |

## Build

### Checkpoint 1: Your Steps

- [ ] **B-cp1.1** (step 1, Get ready): Write down the source and destination account IDs and confirm which identity is in use in Account A.
- [ ] **B-cp1.2** (step 2, Build it): Carry out step 2: create or complete the destination role in Account B, attach the starter permissions policy, and add or complete the permission in Account A, each as the step describes.
- [ ] **B-cp1.3** (step 3, Try it out): Carry out step 3: assume the role and confirm the active identity, list the approved bucket and upload or download a sample file, then attempt one out-of-scope action.
- [ ] **B-cp1.4** (step 4, Fix what's broken): Carry out step 4 when a request returns AccessDenied: work through the first checks the step lists, and note one error and how it was fixed.
- [ ] **B-cp1.5** (step 5, Wrap up): Carry out step 5: explain which policy controls the trust relationship and which controls the S3 permissions, collect the evidence without any credentials in it, and clean up the way the sandbox procedure says.

## Verify

### Checkpoint 1

- [ ] **V-cp1.1** (checks DoD-cp1.1): Check the completed destination trust policy trusts only the approved source identity or role. *Validates B-cp1.2.*
- [ ] **V-cp1.2** (checks DoD-cp1.2): Check the source-side permission lets the source identity assume the exact destination role. *Validates B-cp1.2.*
- [ ] **V-cp1.3** (checks DoD-cp1.3): Check the destination permissions policy and the evidence of the allowed action show the required S3 actions on the target bucket only. *Validates B-cp1.2, B-cp1.3.*
- [ ] **V-cp1.4** (checks DoD-cp1.4): Check one allowed action succeeds and one out-of-scope action is denied, from the role-assumption, S3 and denied-action evidence. *Validates B-cp1.3, B-cp1.4.*
- [ ] **V-cp1.5** (checks DoD-cp1.5): Check the source identity, the trust policy, the role permissions and the temporary credentials can each be described out loud. *Validates B-cp1.1, B-cp1.5.*
- [ ] **V-cp1.6** (checks DoD-cp1.6): Check no long-term access keys were created or shared, no credentials appear in the evidence, and cleanup followed the sandbox procedure. *Validates B-cp1.3, B-cp1.5.*
