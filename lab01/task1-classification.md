# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | It has a fixed 14-week deadline and delivers a unique custom platform for the department. |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | It is an ongoing, repetitive routine process executed daily with no defined end date. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | It is a one-time migration task bound by a strict completion deadline of 15 December. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | It is continuous operational support handled indefinitely according to service level agreements. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | It coordinates three distinct sub-projects to deliver shared strategic integration benefits. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | It is a routine monthly maintenance procedure with no fixed termination point. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | It is a planned future enhancement with a specific target timeframe and unique technical deliverable. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | It represents continuous post-launch maintenance and user support necessary to sustain service. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | It produces a single unique document tied to a specific annual deadline of 31 January. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | It is a hardware deployment effort restricted to the duration of the summer break. |

## Grey zones

1. **Initiative #7 (Multi-node scaling next semester):** This could be classified as a separate project or as ongoing maintenance. Knowing whether it receives separate project charter approval and dedicated funding vs. being pulled from an operational maintenance budget would settle its classification.
2. **Initiative #9 (Annual IT report):** This repeats yearly like an operation, yet produces a unique document against a strict deadline. Knowing whether a dedicated temporary team/budget is authorized each cycle would clarify if it is treated as a project.

## What our project hands over

At go-live in Week 14, the project team transfers system ownership to IT operations, who will manage daily VPS hosting, database backups, monitoring, and user support. To ensure smooth operation, the project team will hand over a production deployment checklist, the verified `docker-compose.prod.yml` configuration, and a comprehensive operations runbook. IT operations will require administrator access tokens, backup verification scripts, and emergency rollback procedures.