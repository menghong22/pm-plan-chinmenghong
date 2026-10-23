# Project charter: Realtime Quiz platform

| Field    | Value                              |
|----------|------------------------------------|
| Version  | 1.0 (draft for sponsor approval)   |
| Date     | 2026-09-29                         |
| Sponsor  | Head of the IT department          |
| PM       | Supervising lecturer               |

## 1. Purpose and justification
Instructors face heavy manual marking loads and lack real-time student engagement feedback during lectures. The Realtime Quiz platform provides an automated, web-based live assessment tool enabling real-time scoring, instant student feedback, and automated leaderboard generation. By implementing this system, the department expects to save significant instructor evaluation time while modernizing classroom interaction. Full financial and operational justification is documented in `business-case.md`.

## 2. Objectives and success criteria

| #  | Objective (what will be true) | Success criterion (number + week) |
|----|------------------------------------|-----------------------------------|
| O1 | Deploy core MVP feature set for live quiz execution | 100% of Must-have features demonstrated with 0 critical defects by week 7 |
| O2 | Conduct live pilot evaluation with students | 50 participants completing a live session with 0 blocking issues in week 14 |
| O3 | Maintain acceptable real-time WebSocket latency | Broadcast latency <= 500 ms at the 95th percentile under load in week 14 |
| O4 | Verify server resource capacity for target usage | 1 server instance sustaining 20 sessions of 100 users on 2 vCPU / 2GB RAM in week 13 |
| O5 | Ensure codebase quality and stability via automated testing | Test suite maintaining >= 80% line coverage with green CI pipeline by week 14 |

## 3. High-level scope

In scope:
- Instructor quiz authoring interface for multiple-choice questions
- Real-time student participation system with 6-character session entry codes
- Real-time scoring, authoritative countdown timers, and live leaderboards over WebSocket
- Role-based authentication system supporting Instructor, Student, and Guest roles
- Quiz results export module supporting CSV and PDF formats

Out of scope:
- Native mobile applications for iOS or Android
- Non-multiple-choice question formats (such as free text or code submission)
- Integrated video conferencing or live audio streaming
- LMS (Learning Management System) integration or multi-node server scaling

## 4. Milestones

| Week | Milestone | Ends process group |
|------|------------------------------------|--------------------|
| 1 | Project charter approved and team assigned | Initiating |
| 3 | Requirements baseline and architecture design finalized | Planning |
| 7 | MVP demo successfully presented | Executing |
| 10 | Analytics, reporting, and export capabilities completed | Executing |
| 13 | Load testing at 100 simulated users passed; deployment ready | Executing / Controlling |
| 14 | Live pilot with 50 students completed successfully | Executing |
| 14 | Final project hand-over, documentation, and formal closure | Closing |

## 5. Budget summary

Effort:  students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h  
Cash:    hosting 4 x 25 USD = 100 USD; domain 15 USD; tools 60 USD; reserve 25 USD (14 %); total 200 USD

## 6. Assumptions
- Students will access the application using their own web-enabled mobile devices or laptops during live sessions.
- Linode VPS infrastructure and domain registration remain accessible and operational throughout the 14-week project window.
- The supervising lecturer is available for 3 hours per week to conduct status reviews and provide technical governance.

## 7. Constraints
- Strict project completion timeline of 14 weeks starting from 2026-09-29.
- Maximum total cash expenditure hard capped at 200 USD.
- Total student team effort limited to 448 person-hours across the semester.

## 8. High-level risks
- Campus proxy networks may block standard WebSocket connections, requiring a SockJS fallback mechanism.
- Client system clock drift relative to the server may compromise timer accuracy, necessitating server-authoritative time checks.
- PDF generation libraries may fail to render Khmer text characters correctly in exported summary reports.

## 9. Project manager authority
The Project Manager is authorized to reallocate student task assignments and adjust internal schedule buffers within the 490 total hours and 200 USD budget. Any proposed additions to scope, schedule extensions beyond week 14, or budget expenditures exceeding the 25 USD reserve require written sponsor approval.

## 10. Approval

Sponsor: ___________________________ Date: ____________  
PM: ___________________________ Date: ____________