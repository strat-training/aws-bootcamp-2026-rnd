# Checkpoint 1: The Account Access Challenge: Instructor Notes

*For instructors only. Do not share with trainees. The trainee handout is [`cp1-brief.md`](cp1-brief.md).*

**Before the trainee starts**
- [ ] Sandbox 3 and Sandbox 4 are mapped to Account A and Account B, confirmed against the access that was provisioned.
- [ ] Each trainee has a working identity or role in the source sandbox, and has the account IDs and role names for both accounts.
- [ ] The destination bucket exists, or the trainee may create it.
- [ ] The starter trust-policy JSON and the permissions-policy example are ready, with clear placeholders.
- [ ] A clear record shows which identity may assume the destination role.
- [ ] Role creation and role assumption are confirmed as permitted in both sandboxes.
- [ ] Expected results and pass conditions are written down: the five pass conditions and the safety check in section 4 of the brief.
- [ ] Cleanup steps are tested.

**Decide before the trainee starts:** the sandbox direction if the administrator provisioned the reverse; whether the trainee or the instructor creates the destination bucket; which pass conditions count as critical (the source marks none, and this brief treats all five as critical); what a trainee submits as the error note if no error occurs; and how deep the written explanations should be.

**Hints and common mistakes:** the AWS tutorial on cross-account roles is the primary implementation guide, and the supplementary article is optional pre-reading. If role assumption fails, the first checks are the active source identity, the source permission for the exact role ARN, the destination trust policy and the account IDs. Watch for a trust policy wider than the approved source identity or role, S3 actions broader than the required ones, and long-term access keys.

**Suggested schedule (the Day 4 activity block)**

| Activity | Time |
|---|---:|
| Activity work | 3 hours 30 minutes |
| Troubleshooting and review | 45 min |
| Wrap-up and cleanup | 30 min |
