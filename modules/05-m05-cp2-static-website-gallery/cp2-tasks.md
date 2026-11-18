# Checkpoint 2: The Cloud Photo Gallery: Tasks

**Objective:** Publish the provided gallery files as a static website from a dedicated S3 bucket, and open it in a browser.

> There is no solutions file for this checkpoint. This checklist guides the work, it does not contain it. Source of every task: [`cp2-brief.md`](cp2-brief.md). A checkpoint brief has no Scope table and no Research column, so there are no research tasks. Its hand-in items are listed in section 5 of the brief and are not tasks. The optional Lambda extension is never a pass requirement, so no verify task checks it.

> **Region:** do all of this in Asia Pacific (Singapore), `ap-southeast-1`.

## ID scheme

| Prefix | Meaning | Source in the brief |
| --- | --- | --- |
| `B-cp2.<step>` | Build task | One per row of the Your Steps table (section 3) |
| `B-cp2.O<n>` | Optional build task | One per row of the optional Lambda thumbnail extension table, marked optional |
| `V-cp2.<n>` | Verify task, checks `DoD-cp2.<n>` | The n-th row of the How You'll Know You're Done table (section 4) |

## Traceability

| Step | Build | Verify (DoD) |
| --- | --- | --- |
| 1. Get ready | B-cp2.1 | V-cp2.1 (DoD-cp2.1) |
| 2. Build it | B-cp2.2 | V-cp2.1, V-cp2.2, V-cp2.4, V-cp2.5 (DoD-cp2.1, DoD-cp2.2, DoD-cp2.4, DoD-cp2.5) |
| 3. Try it out | B-cp2.3 | V-cp2.2, V-cp2.3 (DoD-cp2.2, DoD-cp2.3) |
| 4. Fix what's broken | B-cp2.4 | V-cp2.3 (DoD-cp2.3) |
| 5. Wrap up | B-cp2.5 | V-cp2.4, V-cp2.5 (DoD-cp2.4, DoD-cp2.5) |
| Optional extension | B-cp2.O1, B-cp2.O2, B-cp2.O3, B-cp2.O4, B-cp2.O5, B-cp2.O6 | none (never a pass requirement) |

## Build

### Checkpoint 2: Your Steps

- [ ] **B-cp2.1** (step 1, Get ready): Carry out step 1: create the dedicated gallery bucket in the Singapore Region and get the starter files.
- [ ] **B-cp2.2** (step 2, Build it): Carry out step 2: upload the website files and the image assets, turn on static website hosting and set the index document, and set up the public read access the step describes.
- [ ] **B-cp2.3** (step 3, Try it out): Carry out step 3: open the website endpoint in a browser and check that the gallery loads and the sample images show.
- [ ] **B-cp2.4** (step 4, Fix what's broken): Carry out step 4 when the site shows AccessDenied or 403, or does not load: work through the first checks the step lists and note what was found.
- [ ] **B-cp2.5** (step 5, Wrap up): Carry out step 5: explain why the direct S3 website endpoint uses HTTP and why it is not the preferred production design, write down which content is public and why the bucket holds only non-sensitive training assets, record the bucket name and Region, and follow the instructor's cleanup instruction.

### Optional extension: generate thumbnails with Lambda

- [ ] **B-cp2.O1** (optional extension step 1): Create a private S3 uploads bucket for the original images.
- [ ] **B-cp2.O2** (optional extension step 2): Configure an S3 ObjectCreated event to invoke the prepared Lambda function.
- [ ] **B-cp2.O3** (optional extension step 3): Use a Lambda execution role with only the read, write and logging permissions it needs.
- [ ] **B-cp2.O4** (optional extension step 4): Write the generated thumbnails to the gallery bucket.
- [ ] **B-cp2.O5** (optional extension step 5): Review the Lambda run in CloudWatch Logs.
- [ ] **B-cp2.O6** (optional extension note): Keep the input and output buckets separate, so recursive S3-triggered invocations are avoided.

## Verify

### Checkpoint 2

- [ ] **V-cp2.1** (checks DoD-cp2.1): Check the index file, the styles and the image assets are in the correct gallery bucket. *Validates B-cp2.1, B-cp2.2.*
- [ ] **V-cp2.2** (checks DoD-cp2.2): Check the S3 website endpoint loads the index document. *Validates B-cp2.2, B-cp2.3.*
- [ ] **V-cp2.3** (checks DoD-cp2.3): Check the sample images show correctly when the gallery is opened in a browser. *Validates B-cp2.3, B-cp2.4.*
- [ ] **V-cp2.4** (checks DoD-cp2.4): Check there is an explanation of public access, why the content is non-sensitive sample content, and the production alternative. *Validates B-cp2.2, B-cp2.5.*
- [ ] **V-cp2.5** (checks DoD-cp2.5): Check public read is limited to this training bucket and to `s3:GetObject`, nothing public can be uploaded or deleted, there is no confidential or personal information, and cleanup followed the instructor's instruction. *Validates B-cp2.2, B-cp2.5.*
