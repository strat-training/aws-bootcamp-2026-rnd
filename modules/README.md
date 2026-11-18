# AWS 2-Week Bootcamp: Build-to-Teach Modules

Each folder here is one stage of the bootcamp. The trainee builds the stage and writes it up at the same time, so the finished pair, a working build and a guide another trainee could follow, can go into the content library for the next cohort. The framework is in [`../docs/build-to-teach-framework.md`](../docs/build-to-teach-framework.md). The source is [`../docs/arch-docs/AWS_2_Week_Bootcamp_Curriculum_Entry_Level.md`](../docs/arch-docs/AWS_2_Week_Bootcamp_Curriculum_Entry_Level.md).

## Order

Stage folders are numbered in the order they are done, and folders `01` to `10` match modules `m01` to `m10`. A lecture sits in the same folder as the activity that follows it, so `m03` and `cp1` share `03-m03-cp1-...`, and `m05` and `cp2` share `05-m05-cp2-...`. The last checkpoint has its own folder, `11-cp3-...`, after `m10`. The source's three assessed activities are the three checkpoints. The source has no separate capstone, so there is no `CAPSTONE.md`.

## The cycle

1. **The trainer hands over the brief.** `brief.md` states the objective, scope, stack constraints, labs and deliverable. It contains no lessons and no answers: the trainee designs and builds the stage.
2. **The trainee builds and writes up the stage together.** Copy `write-up-template.md` to `write-up.md` and fill it in as the work goes, not afterwards.
3. **Both get reviewed together.** The trainer reviews the build against the lab Acceptance rows and the write-up for whether it is teachable, stage by stage, before the trainee moves on.
4. **The trainee revises** based on that review.
5. **The finished pair goes into the content library.** The trainer decides what carries into the next cohort.

## What is in a stage folder

A folder that pairs a lecture with its activity holds both, with each file prefixed by its part: `m03-brief.md`, `cp1-brief.md`, `cp1-instructor-notes.md`, `m03-tasks.md`, and so on. Every other folder uses the plain names below.

| File | Written by | Purpose |
| --- | --- | --- |
| `brief.md` | Trainer | Curriculum handoff: objective, scope with time, stack constraints, labs with Acceptance rows, deliverable, open questions. The checkpoint briefs use the learner-facing checkpoint format instead |
| `instructor-notes.md` | Trainer | Checkpoints only (`cp1-instructor-notes.md`, `cp2-instructor-notes.md`, and `instructor-notes.md` in `11-cp3-...`): the instructor-only preparation checklist, decisions to make before the trainee starts, hints and schedule. Not shared with trainees |
| `write-up-template.md` | Trainer | Blank write-up (module stages only), with the stage's questions, concept topics and evidence requests filled in |
| `write-up.md` | Trainee | The trainee's own write-up, copied from the template and filled in during the build |
| `tasks.md` | Generated | Checklist bridging the brief and the write-up, produced by `/trainee-task-planner`. Generated for every stage, but `m03-tasks.md` and `m05-tasks.md` hold research tasks only until their lab and definition of done exist |

## Definition-of-done IDs

A module stage has one lab and uses `DoD-<stage>.<n>`: the n-th sentence of the Acceptance row of that stage's lab, for example `DoD-m07.4` is the fourth clause of the `m07` lab. A checkpoint uses `DoD-cp<n>.<k>`, typed in the table in section 4 of its brief. The same ID is used in the brief, in the verify tasks and in the write-up evidence.

## Stages

| Folder | Stage | Time | Lab |
| --- | --- | --- | --- |
| `01-m01-aws-fundamentals/` | AWS Fundamentals | 6.75 h | 1 lab, 5 steps, 4 Acceptance clauses |
| `02-m02-iam-fundamentals/` | IAM Fundamentals | 6.75 h | 1 lab, 4 steps and 1 optional, 6 Acceptance clauses |
| `03-m03-cp1-cross-account-iam/` (`m03-`) | Cross-Account IAM Access | 2.0 h | **draft, awaiting review:** 1 lab, 4 steps and 1 optional, 6 Acceptance clauses |
| `03-m03-cp1-cross-account-iam/` (`cp1-`) | The Account Access Challenge (Checkpoint 1) | 4.75 h | checkpoint: 5 steps, 6 checks |
| `04-m04-s3-and-cloud-storage/` | S3 and Cloud Storage | 6.75 h | 1 lab, 5 steps, 6 Acceptance clauses |
| `05-m05-cp2-static-website-gallery/` (`m05-`) | Static Website Hosting and Serverless | 2.0 h | **draft, awaiting review:** 1 lab, 5 steps, 5 Acceptance clauses |
| `05-m05-cp2-static-website-gallery/` (`cp2-`) | The Cloud Photo Gallery (Checkpoint 2) | 4.75 h | checkpoint: 5 steps and a 5-step optional extension, 5 checks |
| `06-m06-networking-fundamentals/` | Networking Fundamentals | 3.25 h | 1 lab, 4 steps and 1 optional, 6 Acceptance clauses |
| `07-m07-compute-fundamentals/` | Compute Fundamentals | 3.5 h | 1 lab, 7 steps and 1 optional, 6 Acceptance clauses |
| `08-m08-monitoring-and-operations/` | Monitoring and Operations | 1.5 h | 1 lab, 5 steps and 1 optional, 6 Acceptance clauses |
| `09-m09-aws-services-and-architecture/` | AWS Services and Architecture Overview | 1.25 h | 1 lab (written exercise), 5 steps, 4 Acceptance clauses |
| `10-m10-iac-and-cloudformation/` | Infrastructure as Code and CloudFormation Fundamentals | 4.0 h | 1 lab, 6 steps, 5 Acceptance clauses |
| `11-cp3-one-click-infrastructure/` | One-Click Infrastructure (Checkpoint 3) | 13.5 h | checkpoint: 5 steps, 6 checks |
| | **Total** | **60.75 h** | nine 6.75-hour working days, Days 2 to 10 |

## Notes

- **Day 1 is not a stage.** The source makes it an onboarding and sandbox-access buffer and says not to depend on it for core instruction.
- **The hours are drafts for the trainer to approve.** The source gives per-module time only for Days 7 and 8 (`m06` to `m10`). Those two days each total 6.75 h (8 h less 1.25 h of breaks), so that is the working day used everywhere else. On Days 4 and 6 the day is split using the source's generic daily plan: the concepts and demonstration blocks (2.0 h) go to the module, and the activity block, troubleshooting and review, and wrap-up (4.75 h) go to the checkpoint. The split inside each stage, between subjects, is a draft. The course is self-paced, so there are no instructor demonstrations: the source's demonstration time is self-study of the reference reading.
- **The Research questions are drafts.** The source has none. Each is written from the source's own topics for the trainer to edit.
- **One lab per module stage, as in the source's guided practice,** chunked by subject through the Lab chunk column. Conditional steps ("if enabled", "if the sandbox permissions allow") are Optional rows and are not in the Acceptance row. The source's instructor demonstrations were dropped. The five guided-discussion items of `m09` are its lab steps, done as a written exercise. The source's single "Expected output" sentence per module is split into checkable clauses, and where it does not cover a step the clause restates what that step produces.
- **Checkpoints** follow `docs/templates/Checkpoint_Template.md`. They are the learner-facing handouts, so they speak to the learner as "you", while the module briefs are trainer handoffs written about "the trainee". The instructor-only material sits in a separate instructor-notes file beside each brief, so the brief can be handed to trainees as it is. Checkpoints have no write-up template. Their definition of done is the source's Pass-criteria rows, and three clauses were added from other lines of the source: `DoD-cp1.6` (no long-term access keys, from the source's guardrails), `DoD-cp2.5` (public access scoped to `s3:GetObject` on the training bucket, from step 5) and `DoD-cp3.6` (the trainee explains the template, from step 10 and the required submission). The source gives no weights and no pass mark beyond its PASS, RETRY REQUIRED and NOT YET DEMONSTRATED rules, so the checkpoints use those. It does not say which pass conditions are critical, so the briefs treat all of them as critical and list it as a decision for the instructor.
- **The three reference architectures** are embedded in the checkpoint briefs because the source shows them to learners and asks cp1 for an annotated copy of Figure 1.
- **The Region is Asia Pacific (Singapore), `ap-southeast-1`,** as set by the trainer. It is stated in the header of every brief and tasks file, so trainees see it before they start. The source leaves the Region blank.
- **Instructor-provided values** (sign-in method, AMI, instance type, VPC and subnet IDs, account IDs, the Sandbox 3 to Sandbox 4 direction, bucket naming) are listed as open questions in the briefs. They are not filled in here.
- **The source's learning-reference links** are carried into each brief as a Reference reading row (in Stack constraints for modules, and in Before You Start for checkpoints), because in a self-paced course they are the study material. The `cp2` row leaves out the CloudFront link the source lists, since `cp2` asks the learner to explain the production alternative.

### Needs the trainer

- **`m03` and `m05` are drafts awaiting review.** The source gives each only a one-line focus and then the checkpoint activity, with no learning objective, core topics, guided practice or expected output. Their objective, lab, Acceptance row and deliverable were drafted from the program outcomes, the daily plan and the activity text, and each brief ends with review notes naming the source of every item and the judgements to confirm. Both labs are study labs built from the reference figure, the starter files, the reference reading and the troubleshooting guide. They create no cloud resources, because the source gives the hands-on block to the checkpoint. Their write-up templates (`m03-write-up-template.md`, `m05-write-up-template.md`) are not generated and their tasks files hold research tasks only. Once the drafts are approved, generate the write-up templates and run `/trainee-task-planner re-plan modules/03-m03-cp1-cross-account-iam m03` and `/trainee-task-planner re-plan modules/05-m05-cp2-static-website-gallery m05`. The part name is needed because each of those folders holds two parts.
- **A program outcome has no required hands-on lab:** *explain how an S3 event can invoke Lambda to process an uploaded file* appears in the source only in the optional thumbnail extension of `cp2`, which must not become a pass requirement. The `m05` draft covers it by an explanation and reading (its Acceptance clauses 4 and 5). Making a hands-on Lambda step required is a decision for the trainer.

### Source inconsistencies to confirm

- The troubleshooting order differs on identity versus Region between the Module 8 topic list and the source's beginner troubleshooting sequence. `m01` follows the sequence (account and Region first), and `m08` lists the conflict as an open question.
- The source lists the Day 10 instructor checklist among the trainee's required submissions for Activity 3. `cp3` keeps it on the instructor side.
- `m08` step 1 reviews EC2 metrics, but `m07` terminates its instance unless the instructor designates it for reuse. `m08` lists this as an open question.
