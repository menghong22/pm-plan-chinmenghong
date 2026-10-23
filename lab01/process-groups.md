# Process Groups Mapping and Phase Gates

## Process groups over the semester

| Process group | Weeks active | Main activities | Outputs | Lab that produces them |
|---------------|--------------|-----------------|---------|------------------------|
| Initiating | 1 | Define purpose, write charter, identify stakeholders, construct business case | Project charter, initial stakeholder register, business case | Lab 01 |
| Planning | 1-3 (ongoing) | Scope definition, WBS construction, schedule estimation, risk and communication planning | PM plan, subsidiary plans, baselines | Labs 02-04 |
| Executing | 3-14 | Core system development, UI implementation, analytics, load testing | Working software releases, MVP build, pilot execution | Labs 05-08 |
| Monitoring and controlling | 1-14 | Track schedule/cost variances, review risks, manage change requests | Weekly status reports, change log, updated baselines | Labs 05-10 |
| Closing | 14 | Execute student pilot, conduct final handover, compile lessons learned | Final lab record, deployment runbook, post-project evaluation | Lab 12 |

```mermaid
gantt
  title Process groups over the 14-week semester (Realtime Quiz)
  dateFormat YYYY-MM-DD
  axisFormat %d %b
  section Initiating
  Charter, stakeholders, business case   :i1, 2026-09-29, 7d
  section Planning
  PM plan and subsidiary plans           :p1, 2026-09-29, 21d
  Re-planning after each status review   :p2, 2026-10-20, 56d
  section Executing
  Build to MVP (Must features)           :e1, 2026-10-13, 35d
  MVP demo                               :milestone, m1, 2026-11-13, 0d
  Should and Could features, hardening   :e2, 2026-11-14, 28d
  section Monitoring and controlling
  Weekly status, variance, change log    :m2, 2026-09-29, 98d
  section Closing
  Pilot with 50 students, lessons learned :c1, 2026-12-22, 14d
  Pilot demo                             :milestone, m2, 2026-12-29, 0d