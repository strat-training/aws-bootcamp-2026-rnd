# m04: S3 and Cloud Storage: Tasks

**Objective:** The trainee creates and uses an S3 bucket, manages sample objects including a revised version of one object, and explains the difference between private storage and public website content and why public access must be carefully scoped.

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
| 4.1 Buckets, objects and keys | R-4.1 | B-m04.1, B-m04.2 | V-m04.1, V-m04.2 (DoD-m04.1, DoD-m04.2) |
| 4.2 Versioning, encryption and lifecycle concepts | R-4.2 | B-m04.3 | V-m04.3 (DoD-m04.3) |
| 4.3 Access control: Block Public Access and bucket policies | R-4.3 | B-m04.4 | V-m04.4, V-m04.6 (DoD-m04.4, DoD-m04.6) |
| 4.4 Static website hosting and the production alternative | R-4.4 | B-m04.5 | V-m04.5 (DoD-m04.5) |

## Research

- [ ] **R-4.1** (Scope 4.1): Answer in writing: which decisions are made when naming a bucket and choosing its Region, and why do they matter? Look in the Amazon S3 documentation on buckets, bucket naming and objects.
- [ ] **R-4.2** (Scope 4.2): Answer in writing: when is versioning worth its extra storage, and which problem does a lifecycle rule address? Look in the Amazon S3 documentation on versioning and on lifecycle management.
- [ ] **R-4.3** (Scope 4.3): Answer in writing: why must public access be carefully scoped, and what should be checked before any bucket content is made public? Look in the Amazon S3 documentation on access management.
- [ ] **R-4.4** (Scope 4.4): Answer in writing: which S3 settings would change for direct static website hosting, and why is that not the preferred production design? Look in the Amazon S3 documentation on hosting a static website, and finalise after B-m04.5.

## Build

### Lab m04: Create a bucket and manage objects

- [ ] **B-m04.1** (Lab m04 step 1): Create a uniquely named training bucket.
- [ ] **B-m04.2** (Lab m04 step 2): Upload and download sample files using the Console.
- [ ] **B-m04.3** (Lab m04 step 3): Enable versioning and upload a revised version of one sample file.
- [ ] **B-m04.4** (Lab m04 step 4): Inspect Block Public Access and a sample bucket policy.
- [ ] **B-m04.5** (Lab m04 step 5): Identify which S3 settings would need to change for direct static website hosting, without disabling protections on any bucket outside the training exercise.

## Verify

### Lab m04

- [ ] **V-m04.1** (checks DoD-m04.1): Check the training bucket exists with a unique name in the Singapore Region. *Validates R-4.1, B-m04.1.*
- [ ] **V-m04.2** (checks DoD-m04.2): Check sample files are uploaded and downloaded through the Console. *Validates B-m04.2.*
- [ ] **V-m04.3** (checks DoD-m04.3): Check versioning is enabled and the previous version of the revised file is identified. *Validates R-4.2, B-m04.3.*
- [ ] **V-m04.4** (checks DoD-m04.4): Check the Block Public Access settings and the sample bucket policy are inspected and described. *Validates R-4.3, B-m04.4.*
- [ ] **V-m04.5** (checks DoD-m04.5): Check the S3 settings that would need to change for direct static website hosting are identified, and that no protection was disabled on any other bucket. *Validates R-4.4, B-m04.5.*
- [ ] **V-m04.6** (checks DoD-m04.6): Check there is an explanation of why public access must be carefully scoped. *Validates R-4.3, R-4.4, B-m04.4, B-m04.5.*
