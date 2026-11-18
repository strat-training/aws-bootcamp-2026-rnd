# m05: Static Website Hosting and Serverless Fundamentals

**Schedule:** Day 6 (study part) · **Builds on:** `04-m04-s3-and-cloud-storage` · **Feeds into:** [`cp2-brief.md`](cp2-brief.md), the activity in this folder · **Region:** Asia Pacific (Singapore), `ap-southeast-1`

> **DRAFT for trainer review. Nothing here is approved.** The source gives this module only a one-line focus (*static website concepts, HTML/CSS deployment, S3 website hosting, public versus private content, Lambda fundamentals, event triggers, S3 notifications, and CloudWatch Logs*). The Objective, Lab, Acceptance row and Deliverable below are drafted from the source's program outcomes, its Day 6 plan, its reference reading and Activity 2 (`cp2`). The course is self-paced, so there is no instructor demonstration. The sources and the judgements to confirm are in the review notes at the end. Delete this banner and those notes once approved.

## Objective

By the end of this stage, the trainee explains how a static website is served from an S3 bucket and which content is public and which stays private, and explains how an upload to S3 can invoke a Lambda function, what the function needs and where its run is logged, ready to publish the gallery in `cp2`.

## Scope

The hours are drafts: the source's generic daily plan sets aside 120 minutes for concepts and demonstration ahead of the activity block, which `cp2` takes. With no instructor demonstration, that time is self-study of the reference reading. The Research questions are drafts.

| # | Subject | Time | Key concepts and terms | Research | Lab chunk |
| --- | --- | --- | --- | --- | --- |
| 5.1 | Static website concepts and S3 website hosting | 1.0 h | static website, HTML/CSS deployment, S3 website hosting, website endpoint, public versus private content | What makes content safe to serve from a public S3 website endpoint, and what must stay private? | Steps 1–3: Trace the gallery and sort its content |
| 5.2 | Lambda, event triggers and logs | 1.0 h | AWS Lambda, event trigger, S3 notification, execution role, CloudWatch Logs | What has to be configured for an S3 upload to run a Lambda function, and where does the trainee look to see whether it ran? | Steps 4–5: Trace the thumbnail workflow and read the tutorial |
| | **Total** | **2.0 h** | | | |

## Stack constraints

| Constraint | Detail |
| --- | --- |
| Inherited | Same as m01: sandbox accounts, authentication, data, cost control, cleanup and troubleshooting order. |
| Public content | Direct S3 website hosting needs public access and supports HTTP only. It is limited to a dedicated training bucket holding sample, non-sensitive assets. |
| Lambda | Concepts and reading only. Custom Python development is not required, and code packaging is never a pass requirement. |
| Provided material | The reference architecture figure and the starter files (`index.html`, the CSS and the sample images) that `cp2` uses. |
| Scope | Study only. No resources are created in this stage, and the hands-on gallery build is `cp2`. |
| Reference reading | The study material for this self-paced stage: [S3 static website tutorial](https://docs.aws.amazon.com/AmazonS3/latest/userguide/HostingWebsiteOnS3Setup.html), [Lambda S3 thumbnail tutorial](https://docs.aws.amazon.com/lambda/latest/dg/with-s3-tutorial.html), [CloudFront secure static website](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/getting-started-secure-static-website-cloudformation-template.html). |

## Lab

This stage has one lab, built up in chunks. The Lab chunk column in the Scope table shows which steps practise each subject. The Acceptance row is what the trainer checks.

### Lab m05: Trace the gallery and the thumbnail workflow

| Step | What the trainee does |
| --- | --- |
| 1 | Studies the reference architecture figure and names each element of the required path: the browser, the S3 website bucket holding the index file, the CSS and the images, and the website endpoint, with the protocol between them. |
| 2 | Opens the starter files that `cp2` uses and identifies the stylesheet and the images that the index file refers to. |
| 3 | Sorts the files the gallery needs, and the private uploads bucket of the thumbnail workflow, into content that is public for the website and content that stays private, and states the reason for each. |
| 4 | Names each element of the optional thumbnail workflow in the reference architecture figure, and traces in order what happens when an image is uploaded to the private uploads bucket. |
| 5 | Reads the Lambda S3 thumbnail tutorial and records what starts the function, which permissions its execution role needs, and where its run is logged. |
| **Acceptance** | Each element of the required gallery path is named, with the protocol between the browser and the website endpoint. The stylesheet and the images referred to by the index file are identified. The gallery files and the uploads bucket are sorted into public and private, with a reason for each. The trainee explains, in order, how an upload to the private bucket leads to a thumbnail in the gallery bucket through an S3 event and a Lambda function. The trainee states what starts the function, which permissions its execution role needs, and where its run is logged. |

## Deliverable

The deliverable contains:

- [ ] The gallery reference architecture with each element named
- [ ] The list of files the index file refers to
- [ ] The public and private sorting, with a reason for each item
- [ ] The written trace of the upload-to-thumbnail flow
- [ ] Notes from the tutorial: what starts the function, its execution role's permissions and where its run is logged
- [ ] `write-up.md`, filled in from `write-up-template.md`

## Still open / ask the trainer

| Question | Why it matters |
| --- | --- |
| Which reference architecture figure and starter files are handed out in this stage? | Steps 1 to 4, and `cp2` uses the same files |
| Is explanation plus reading enough to cover the Lambda outcome, or should a hands-on Lambda step be required? | The only Lambda checks are Acceptance clauses 4 and 5, and the source makes the hands-on extension optional |
| How deep should the written explanations be? | Avoids over- or under-investing in the write-up |

## Draft review notes (delete once approved)

| Item | Where it comes from | Judgement to confirm |
| --- | --- | --- |
| Objective | The focus line, and the program outcomes *create an S3 bucket, manage sample objects, and publish a basic static website for non-sensitive training content* and *explain how an S3 event can invoke Lambda to process an uploaded file* | It stops at "ready to publish the gallery in `cp2`", because the source puts the build in Activity 2 |
| Lab shape | The Day 6 plan gives the guided-lab block to the Activity and leaves this module only concepts and demonstration time. With no demonstration, the lab is built from the figure, the starter files and the tutorial | The lab creates no cloud resources. The alternative is no lab and a flat `DoD-01`, `DoD-02`, ... list |
| Step 1 | Figure 2 and its caption in Activity 2, including the HTTP label on the website endpoint | |
| Step 2 | The starter files in Activity 2, and "HTML/CSS deployment" in the focus line | An inference: the source gives no step for it. Drop it if you want the files untouched until `cp2` |
| Step 3 | "Public versus private content" in the focus line, and the required explanation of which content is public and why in Activity 2 | |
| Steps 4 and 5 | The optional thumbnail extension in Activity 2 (private uploads bucket, upload event, prepared function, execution role with only the required permissions, review in CloudWatch Logs), and the Lambda S3 thumbnail tutorial in the source's references | Step 5 replaces the instructor demonstration of the first draft. The Lambda outcome still has no required hands-on lab in the source. This draft covers it by explanation and reading (Acceptance clauses 4 and 5). A hands-on step would be stronger, but the source says the extension must not become a pass requirement |
| Acceptance | Clauses 4 and 5 come from the program outcome and the extension. Clauses 1 to 3 restate what steps 1 to 3 produce, because the source gives no module-level expected output | |
