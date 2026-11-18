# Checkpoint 2: The Cloud Photo Gallery: Instructor Notes

*For instructors only. Do not share with trainees. The trainee handout is [`cp2-brief.md`](cp2-brief.md).*

**Before the trainee starts**
- [ ] A simple `index.html`, a CSS file and safe sample images are prepared.
- [ ] The isolated training account allows the bucket-level public-read configuration that this exercise needs, without relaxing protections for other buckets.
- [ ] If the optional extension is offered, tested starter code and its dependencies or package are ready, and packaging is not a pass requirement.
- [ ] Expected results and pass conditions are written down: the four pass conditions and the scoping check in section 4 of the brief.
- [ ] Cleanup steps are tested, including emptying and deleting the bucket.

**Decide before the trainee starts:** whether the optional extension is offered, whether the gallery is shown as a screenshot or live, and how deep the written explanations should be.

**Hints and common mistakes:** if the site shows AccessDenied or 403, the first checks are the website endpoint, the index document, the bucket policy, the Block Public Access settings and the object permissions. If it does not load, check that hosting is enabled, the endpoint is correct and the index file is in the expected location. For production the source recommends a CloudFront distribution with an S3 bucket origin and Origin Access Control, which does not work with an S3 website endpoint. Watch for public write or delete access, relaxed protections on any other bucket, and confidential or personal content.

**Suggested schedule (the Day 6 activity block)**

| Activity | Time |
|---|---:|
| Activity work | 3 hours 30 minutes |
| Troubleshooting and review | 45 min |
| Wrap-up and cleanup | 30 min |
