# Checkpoint 3: One-Click Infrastructure: Tasks

**Objective:** Complete the starter template so one stack creates a web server and its access rule, then deploy it, update it and delete it.

> There is no solutions file for this checkpoint. This checklist guides the work, it does not contain it. Source of every task: [`brief.md`](brief.md). A checkpoint brief has no Scope table and no Research column, so there are no research tasks. Its hand-in items are listed in section 5 of the brief and are not tasks.

> **Region:** do all of this in Asia Pacific (Singapore), `ap-southeast-1`.

## ID scheme

| Prefix | Meaning | Source in the brief |
| --- | --- | --- |
| `B-cp3.<step>` | Build task | One per row of the Your Steps table (section 3) |
| `V-cp3.<n>` | Verify task, checks `DoD-cp3.<n>` | The n-th row of the How You'll Know You're Done table (section 4) |

## Traceability

| Step | Build | Verify (DoD) |
| --- | --- | --- |
| 1. Get ready (Day 9) | B-cp3.1 | V-cp3.6 (DoD-cp3.6) |
| 2. Build it (Day 9) | B-cp3.2 | V-cp3.2, V-cp3.3, V-cp3.4 (DoD-cp3.2, DoD-cp3.3, DoD-cp3.4) |
| 3. Try it out (Day 9 deploy, Day 10 test and update) | B-cp3.3 | V-cp3.1, V-cp3.3, V-cp3.5 (DoD-cp3.1, DoD-cp3.3, DoD-cp3.5) |
| 4. Fix what's broken (as needed) | B-cp3.4 | V-cp3.1 (DoD-cp3.1) |
| 5. Wrap up (Day 10) | B-cp3.5 | V-cp3.5, V-cp3.6 (DoD-cp3.5, DoD-cp3.6) |

## Build

### Checkpoint 3: Your Steps

- [ ] **B-cp3.1** (step 1, Get ready, Day 9): Open the starter YAML file and find its Parameters, Resources and Outputs sections.
- [ ] **B-cp3.2** (step 2, Build it, Day 9): Carry out step 2: complete the Parameters with the values the instructor gives, then define the Security Group, the EC2 instance, the User Data script and the Outputs, each as the step describes.
- [ ] **B-cp3.3** (step 3, Try it out, Day 9 deploy and Day 10 test and update): Carry out step 3: validate the template and deploy the stack, review the stack events until CREATE_COMPLETE, then on Day 10 open the website URL, make one small change, and update the stack after looking at the proposed change in a Change Set where available.
- [ ] **B-cp3.4** (step 4, Fix what's broken, as needed): Carry out step 4 when the stack fails or the page does not load: work through the first checks the step lists, and note what was found.
- [ ] **B-cp3.5** (step 5, Wrap up, Day 10): Carry out step 5: explain the template, its inputs, the resources it created and the network components the instructor prepared in the technical walkthrough, then delete the stack and check that the instance and the Security Group it created are gone.

## Verify

### Checkpoint 3

- [ ] **V-cp3.1** (checks DoD-cp3.1): Check the template validates and the stack reaches CREATE_COMPLETE. *Validates B-cp3.2, B-cp3.3, B-cp3.4.*
- [ ] **V-cp3.2** (checks DoD-cp3.2): Check the template and the stack's resources show that the stack creates the Security Group and the EC2 instance. *Validates B-cp3.2, B-cp3.3.*
- [ ] **V-cp3.3** (checks DoD-cp3.3): Check the User Data installs and starts the web service and the website URL loads. *Validates B-cp3.2, B-cp3.3.*
- [ ] **V-cp3.4** (checks DoD-cp3.4): Check the Security Group rules, in the template and in the Console, enable HTTP for the lab and include no inbound SSH rule. *Validates B-cp3.2.*
- [ ] **V-cp3.5** (checks DoD-cp3.5): Check the stack was updated, with the update and Change Set evidence to show for it, and was deleted, with the instance and the Security Group it created confirmed removed. *Validates B-cp3.3, B-cp3.5.*
- [ ] **V-cp3.6** (checks DoD-cp3.6): Check the template, its inputs, the resources it created and the network components prepared in advance can each be explained in the Day 10 technical walkthrough. *Validates B-cp3.1, B-cp3.2, B-cp3.5.*
