# AWS 2-Week Bootcamp: Build-to-Teach Modules

Each folder in `modules/` is one stage of the bootcamp. The trainee builds the stage and writes it up at the same time,
so the finished pair, a working build and a guide another trainee could follow, can go into the content library for the
next cohort. The framework is in [`docs/build-to-teach-framework.md`](docs/build-to-teach-framework.md) and the source
curriculum is
[`docs/arch-docs/AWS_2_Week_Bootcamp_Curriculum_Entry_Level.md`](docs/arch-docs/AWS_2_Week_Bootcamp_Curriculum_Entry_Level.md).
The course is self-paced, runs for 10 working days, and is done in the training sandboxes in **Asia Pacific (Singapore),
`ap-southeast-1`**.

## Order

Stage folders are numbered in the order they are done, and folders `01` to `10` match modules `m01` to `m10`. A lecture
sits in the same folder as the activity that follows it, so `m03` and `cp1` share `03-m03-cp1-...`, and `m05` and `cp2`
share `05-m05-cp2-...`. The last checkpoint has its own folder, `11-cp3-...`, after `m10`. The source's three assessed
activities are the three checkpoints. The source has no separate capstone, so there is no `CAPSTONE.md`.

## The cycle

1. **The trainer hands over the brief.** `brief.md` states the objective, scope, stack constraints, labs and
   deliverable. It contains no lessons and no answers: the trainee designs and builds the stage.
2. **The trainee builds and writes up the stage together.** Copy `write-up-template.md` to `write-up.md` and fill it in
   as the work goes, not afterwards.
3. **Both get reviewed together.** The trainer reviews the build against the lab Acceptance rows and the write-up for
   whether it is teachable, stage by stage, before the trainee moves on.
4. **The trainee revises** based on that review.
5. **The finished pair goes into the content library.** The trainer decides what carries into the next cohort.

## What is in a stage folder

A folder that pairs a lecture with its activity holds both, with each file prefixed by its part: `m03-brief.md`,
`cp1-brief.md`, `cp1-instructor-notes.md`, `m03-tasks.md`, and so on. Every other folder uses the plain names below.

| File | Written by | Purpose |
| --- | --- | --- |
| `brief.md` | Trainer | Curriculum handoff: objective, scope with time, stack constraints, labs with Acceptance rows, deliverable, open questions. The checkpoint briefs use the learner-facing checkpoint format instead |
| `instructor-notes.md` | Trainer | Checkpoints only (`cp1-instructor-notes.md`, `cp2-instructor-notes.md`, and `instructor-notes.md` in `11-cp3-...`): the instructor-only preparation checklist, decisions to make before the trainee starts, hints and schedule. Not shared with trainees |
| `write-up-template.md` | Trainer | Blank write-up (module stages only), with the stage's questions, concept topics and evidence requests filled in |
| `write-up.md` | Trainee | The trainee's own write-up, copied from the template and filled in during the build |
| `tasks.md` | Generated | Checklist bridging the brief and the write-up, produced by `/trainee-task-planner`. Generated for every stage, but `m03-tasks.md` and `m05-tasks.md` hold research tasks only until their lab and definition of done exist |

## Definition-of-done IDs

A module stage has one lab and uses `DoD-<stage>.<n>`: the n-th sentence of the Acceptance row of that stage's lab, for
example `DoD-m07.4` is the fourth clause of the `m07` lab. A checkpoint uses `DoD-cp<n>.<k>`, typed in the table in
section 4 of its brief. The same ID is used in the brief, in the verify tasks and in the write-up evidence.

## Stages

| Folder (in `modules/`) | Stage | Time | Lab |
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

- Day 1 is onboarding and sandbox access, so it is not a stage. The stages start on Day 2: `m01` is Day 2, `m02` is Day
  3, `m03` with `cp1` is Day 4, `m04` is Day 5, `m05` with `cp2` is Day 6, `m06` and `m07` are Day 7, `m08` to `m10` are
  Day 8, and `cp3` is Days 9 and 10.
- The hours are drafts for the trainer to approve. The source gives per-module time only for Days 7 and 8, so the
  6.75-hour working day those days add up to is used everywhere else, and Days 4 and 6 are split between the module and
  its checkpoint using the source's generic daily plan. The Research questions are drafts too, because the source gives
  none.
- The course is self-paced. There are no instructor demonstrations, so each brief carries the source's
  learning-reference links as its Reference reading.
- Everything is done in Asia Pacific (Singapore), `ap-southeast-1`, as set by the trainer, and the header of every brief
  and tasks file repeats the reminder. The source leaves the Region blank.
- Each module stage has one lab, as in the source's guided practice, and every scope row names its chunk of that lab in
  the Lab chunk column. Conditional steps are Optional rows outside the Acceptance row, and the source's single Expected
  output sentence per module is split into checkable clauses.
- The three checkpoint briefs follow `docs/templates/Checkpoint_Template.md` and are written to the learner as "you",
  while the module briefs are written about "the trainee". Each checkpoint keeps its instructor-only material in a
  separate instructor-notes file, and has no write-up template. Its definition of done is the source's Pass-criteria
  rows, plus `DoD-cp1.6`, `DoD-cp2.5` and `DoD-cp3.6`, which were added from other lines of the source.
- Instructor-provided values (sign-in method, AMI, instance type, VPC and subnet IDs, account IDs, the Sandbox 3 to
  Sandbox 4 direction, bucket naming) are listed as open questions in the briefs. They are not filled in here.
- `m03` and `m05` are drafts awaiting the trainer's review, because the source gives them only a one-line focus. Their
  write-up templates are not generated and their task files hold research tasks only. Once the drafts are approved,
  generate the templates and run `/trainee-task-planner re-plan modules/03-m03-cp1-cross-account-iam m03` and
  `/trainee-task-planner re-plan modules/05-m05-cp2-static-website-gallery m05`.
- The trainer's other open decisions, including the missing hands-on Lambda lab and three inconsistencies in the source,
  are listed under "Needs the trainer" and "Source inconsistencies to confirm" in
  [`modules/README.md`](modules/README.md).
- The commands are `/build-to-teach`, the playbook that generates this structure, and
  `/trainee-task-planner modules/<folder>`, which generates the `tasks.md` checklist for one stage. They live in
  `.claude/`, which is in `.gitignore`, so they do not come with a clone.
