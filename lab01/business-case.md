# Business case: live quizzes for the IT department

## 1. Problem
Instructors spend excessive manual effort grading quizzes and collecting feedback, limiting interactive teaching time during lectures.
Assumptions:
- Lecturers running quizzes: 10
- Marking time saved per lecturer per week: 1 h
- Teaching weeks per year: 30
- Total academic time saved per year: 300 hours
- Notional value of one hour: 10 USD (used for economic evaluation)

## 2. Options

| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A | Do nothing | 0 USD | 0 USD | 0 USD |
| B | Buy commercial SaaS | 0 USD | 1,800 USD | 3,000 USD |
| C | Build Realtime Quiz platform | 4,900 USD | 300 USD | 4,800 USD |

*Note: Option B assumes commercial quiz platform pricing of 15 USD per lecturer per month across 12 months (10 x 15 x 12 = 1,800 USD/year).*

## 3. Comparison

| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers) |
|--------|--------------------|-----------------|----------------------------|
| B | 1,200 USD | 0.00 | 720 USD |
| C | 4,500 USD | 1.09 | 2,700 USD |

## 4. Benefits not priced
- Full institutional ownership and privacy control over student performance data
- Complete customization of features matching local department requirements without user caps
- Valuable hands-on capstone software engineering learning experience for participating students

## 5. Risks per option
- **Option A:** Continued inefficiency, high instructor workload, and low student engagement.
- **Option B:** Vendor lock-in, unpredictable subscription price increases, and external data storage compliance issues.
- **Option C:** Technical delivery delays, potential WebSocket network proxy blocks, and ongoing operational maintenance overhead.

## 6. Recommendation and review gate
**Recommendation:** Proceed with **Option C (Build Realtime Quiz platform)**. Option C yields a net annual benefit of 4,500 USD and achieves financial payback in 1.09 years (or 1.7 years under conservative 6-lecturer sensitivity analysis) while retaining institutional data sovereignty.

**Review Gate:** A formal review gate is set at the **Week 7 MVP Demo**. If the development team fails to deliver the core Must-have features at Week 7, the sponsor should halt custom build spending and transition to Option B (SaaS) for the following academic semester.