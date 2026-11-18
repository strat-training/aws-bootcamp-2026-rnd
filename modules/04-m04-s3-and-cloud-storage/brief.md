# m04: S3 and Cloud Storage

**Schedule:** Day 5 · **Builds on:** `03-m03-cp1-cross-account-iam` · **Feeds into:** `05-m05-cp2-static-website-gallery` · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

## Objective

By the end of this stage, the trainee creates and uses an S3 bucket, manages sample objects including a revised version of one object, and explains the difference between private storage and public website content and why public access must be carefully scoped.

## Scope

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 4.1 | Buckets, objects and keys | 1.75 h | bucket, object, object key, Region, globally unique bucket name, upload, download, organizing files | Which decisions does the trainee make when naming a bucket and choosing its Region, and why do they matter? | Steps 1–2: Create the bucket and move files in and out |
| 4.2 | Versioning, encryption and lifecycle concepts | 1.75 h | versioning, object version, default encryption, lifecycle rule, storage class (concepts only) | When is versioning worth its extra storage, and which problem does a lifecycle rule address? | Step 3: Enable versioning and revise an object |
| 4.3 | Access control: Block Public Access and bucket policies | 1.75 h | Block Public Access, bucket policy, resource-based policy, private versus public content | Why must public access be carefully scoped, and what does the trainee check before any bucket content is made public? | Step 4: Inspect Block Public Access and a bucket policy |
| 4.4 | Static website hosting and the production alternative | 1.5 h | static website hosting, website endpoint, private bucket, CloudFront, Origin Access Control | Which S3 settings would change for direct static website hosting, and why is that not the preferred production design? | Step 5: Identify the settings that would change |
| | **Total** | **6.75 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Tools | The S3 Console. |
| Naming | S3 bucket names are globally unique, so each bucket name needs a unique element. |
| Protections | Block Public Access is inspected, and no protection is disabled on any bucket outside the training exercise. |
| Concepts only | Lifecycle rules and storage classes are covered as concepts. They are not configured. |
| Cleanup | A bucket is emptied before it is deleted. Whether the bucket is kept for later stages is decided by the instructor. |
| Reference reading | The study material for this self-paced stage: [S3 static website tutorial](https://docs.aws.amazon.com/AmazonS3/latest/userguide/HostingWebsiteOnS3Setup.html), [S3 access management](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-management.html), [S3 versioning](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m04: Create a bucket and manage objects

| Step | What the trainee does |
| --- | --- |
| 1 | Creates a uniquely named training bucket. |
| 2 | Uploads and downloads sample files using the Console. |
| 3 | Enables versioning and uploads a revised version of one sample file. |
| 4 | Inspects Block Public Access and a sample bucket policy. |
| 5 | Identifies which S3 settings would need to change for direct static website hosting, without disabling protections on any bucket outside the training exercise. |
| **Acceptance** | The training bucket exists with a unique name in the Singapore Region. Sample files are uploaded and downloaded through the Console. Versioning is enabled and the previous version of the revised file is identified. The Block Public Access settings and the sample bucket policy are inspected and described. The S3 settings that would need to change for direct static website hosting are identified, and no protection was disabled on any other bucket. The trainee explains why public access must be carefully scoped. |

## Deliverable

The deliverable contains:

- [ ] Screenshot of the training bucket, showing its name and Region
- [ ] Screenshot of an uploaded and a downloaded sample file
- [ ] Screenshot of the object versions, with the previous version of the revised file identified
- [ ] Notes on the Block Public Access settings, the sample bucket policy and the settings that would change for static website hosting
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which bucket name prefix or convention applies? | Globally unique naming in lab chunk 4.1 |
| Which sample files and sample bucket policy are provided? | Lab chunks 4.1, 4.2 and 4.3 |
| Is the bucket kept for the next stages or deleted? | Cleanup at the end of the lab |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |
