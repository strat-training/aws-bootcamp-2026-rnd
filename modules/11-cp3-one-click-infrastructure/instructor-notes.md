# Checkpoint 3: One-Click Infrastructure: Instructor Notes

*For instructors only. Do not share with trainees. The trainee handout is [`brief.md`](brief.md).*

**Before the trainee starts**
- [ ] The sandbox permits creating EC2 instances, Security Groups and CloudFormation stacks.
- [ ] The prepared public VPC and subnet route to an Internet Gateway and assign public IPs.
- [ ] The approved AMI ID, the allowed instance type, the VPC ID and the subnet ID are ready to hand out for Singapore (`ap-southeast-1`).
- [ ] The starter YAML file has the basic structure and placeholders.
- [ ] The cleanup procedure and the time limit for the running instance are decided.
- [ ] Expected results and pass conditions are written down: the five pass conditions and the explanation check in section 4 of the brief.
- [ ] Cleanup steps are tested, including removal of the instance and the Security Group.

**Decide before the trainee starts:** the AMI, instance type, VPC and subnet values; the instance time limit; whether Change Sets are available; where the Day 10 walkthrough result is recorded (the source lists the instructor checklist or recorded result among the trainee's submissions, and this brief keeps it on the instructor side); which pass conditions count as critical (the source marks none, and this brief treats all five as critical); and how deep the written explanations should be.

**Hints and common mistakes:** if the stack fails, open the Events tab, find the first resource failure and read its status reason, then check the parameter values and the template syntax. If the page does not load, the first checks are the instance state and status checks, the public IP, the subnet route, the public IP assignment, the Security Group's HTTP rule and the User Data output. Watch for an inbound SSH rule, an instance left running past the time limit, and a trainee building network components that the instructor prepared.

**Suggested schedule**

| Activity | Time |
|---|---:|
| Day 9: build and initial deployment, with the instructor checkpoint | 6.75 hours |
| Day 10: validation, technical walkthrough, update, cleanup and result | 6.75 hours |
