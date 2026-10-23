# Post-mortem: CampusPay wallet project failure (2025)

## 1. Timeline and sources

| # | When | Event | Source |
|---|------|-------|--------|
| 1 | Week 1 | University IT unit asked to build cashless canteen and library payment app in one semester | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |
| 2 | Week 2 | Head of finance "sponsors" project by email but never attends status reviews | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |
| 3 | Week 5 | Scope expands via unmanaged user survey to include bus tickets and parking | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |
| 4 | Week 10 | Lead developer acts as both sole coder and project manager without tracking schedule variance | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |
| 5 | Week 14 | System launched on opening day with zero integration testing against physical card terminals | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |
| 6 | Launch Day+1 | Card terminals reject 40% of transactions, canteen queues double, app crashes | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |
| 7 | Launch Day+3 | Application withdrawn from service under heavy student and administrative criticism | Fictional case from [Lab-01](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#challenge) [cite: [Lab-01 · Introduction to project management](https://gicitc.com/courses/it-project-management/01-IntroductionToProjectManagement/Lab-01.html#top)] |

## 2. Classification and organisation

- **Project / Programme:** It was treated as a single unstable project that suffered from unmanaged sub-components.
- **Structure and PM authority:** The project operated under a dysfunctional functional/hierarchical structure where the lead developer doubled as project manager with zero formal management authority or administrative backing.
- **Sponsor, charter, PMO:** There was no formal signed charter, no Project Management Office (PMO) oversight, and the nominal sponsor (head of finance) exercised passive support via email without active governance.

## 3. Success criteria

- **Stated:** "Launch in September."
- **Missing measurable criteria:** No explicit performance targets for transaction success rate, concurrent user capacity, latency limits, or hardware error thresholds.
- **Ignored dimensions:** Operational stability, user experience under load, team sustainability, and long-term benefit realization were completely ignored in favor of an arbitrary calendar deadline.

## 4. Process groups and knowledge areas

| Process group | What went wrong or was skipped |
|----------------------------|--------------------------------|
| Initiating | No formal project charter was signed, leaving scope and sponsorship completely undefined. |
| Planning | Requirements grew unchecked via surveys without a formal change control board or WBS baseline. |
| Executing | Development proceeded without integration testing against real physical hardware terminals. |
| Monitoring and controlling | Progress was falsely reported as "on schedule" without quality metrics or risk reviews (the invisibility trap). |
| Closing | The project abruptly collapsed into an emergency withdrawal rather than a controlled, evaluated closure. |

**Knowledge areas most responsible:** 
1. *Integration Management* (due to total lack of coordination and holistic project control).
2. *Scope Management* (due to uncontrolled scope creep from unvetted feature requests).
3. *Quality Management* (due to skipping end-to-end hardware testing prior to go-live).

## 5. Ethics

- **Decision examined:** Releasing the payment application to production without conducting terminal integration tests.
- **Evaluation against PM values:** 
  - *Responsibility:* Violated by knowingly deploying untested financial software that risked user funds and data.
  - *Respect:* Disrespected end users (students and canteen staff) by exposing them to system failures and long queues.
  - *Fairness:* Violated by placing the entire blame on low-level developers when governance structures failed.
  - *Honesty:* Violated when status reports falsely claimed the project was "on schedule" despite systemic hardware incompatibilities.

## 6. What our project will do differently

| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | We will run a live session with 100 simulated students over real campus Wi-Fi before deploying | Load test report with 0 critical errors | Week 12 | Objective O3 (latency) & Milestone Week 13 |
| 2 | We will maintain a signed project charter with a named sponsor who actively attends milestone gates | Signed document & gate review minutes | Week 1 | Section 10 Approval block & Authority clause |
| 3 | We will process all scope additions through a formal change request log evaluated by the PM | Change log document in repository | Weekly (Weeks 2–13) | Section 9 PM Authority rules |
| 4 | We will execute automated test suites maintaining at least 80% line coverage on every pull request | Green CI pipeline status badge | Week 14 | Objective O5 (code quality) |
| 5 | We will produce a complete operations runbook and verify database backups before launch | Runbook file & IT operations sign-off | Week 13 | Task 1 Handover requirements & Milestone Week 14 |