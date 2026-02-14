# Tech Lead Performance Dashboard

---

## 🧱 Team Delivery

| Indicator | Target | Current | Trend |
|---|---|---|---|
| Sprint Commitment (%) | >85% | | ↑ / ↓ |
| Average Lead Time | Decreasing | | ↑ / ↓ |
| Blockers Removed | >3 per week | | ↑ / ↓ |

### Definitions

**Sprint Commitment (%)**
The percentage of planned story points or tasks actually completed by the end of the sprint. Measures how predictable the team's delivery is.

> Example: The team committed to 40 story points and delivered 36. Sprint commitment = 90%. This tells the manager that estimates are reliable and the team is not overcommitting.

**Average Lead Time**
The elapsed time from when work starts on a task (moved to "In Progress") to when it reaches production. Lower is better.

> Example: A task was picked up on Monday and deployed on Thursday. Lead time = 4 days. If the team average drops from 6 days to 4 days over a month, the trend is positive.

**Blockers Removed**
The number of impediments you actively resolved or escalated for the team in a given week. Includes technical, process, or cross-team blockers.

> Example: You unblocked a developer waiting on API access by escalating to the platform team. You resolved a CI pipeline flake that was holding up PRs. You clarified ambiguous requirements with the PM before the team wasted effort. That's 3 blockers removed.

---

## 🏗 Quality & Architecture

| Indicator | Target | Current |
|---|---|---|
| Technical Debts Addressed | 1-2 per sprint | |
| Critical Incidents | 0 | |
| RFCs Proposed | 1 per month | |

### Definitions

**Technical Debts Addressed**
Concrete improvements to code quality, architecture, or infrastructure that reduce future risk or maintenance cost. These should be intentional, not accidental side effects.

> Example: Refactored the payment validation logic from a 400-line method into smaller, testable functions. Or: Replaced a deprecated library dependency before it became a security risk. Each counts as one debt addressed.

**Critical Incidents**
Production incidents that caused user-facing impact, data loss, or required emergency intervention. The target is zero — your job is to prevent these through risk anticipation and quality gates.

> Example: A deployment caused 500 errors for 15 minutes affecting checkout. That's 1 critical incident. A background job failed silently but had no user impact — that's not critical, but should still be tracked and fixed.

**RFCs Proposed**
Request for Comments — written proposals for architectural or process changes shared with the team for discussion. Shows you are thinking ahead and driving technical direction.

> Example: You write a one-page document proposing the team adopt a circuit breaker pattern for external API calls, outlining the problem, options, and recommendation. The team discusses it in a meeting and agrees on an approach.

---

## 🤝 Influence

| Indicator | Target | Current |
|---|---|---|
| Structured Code Reviews | 8+ per week | |
| Mentorship Sessions | 1-2 per week | |
| Onboarding Support | As needed | |

### Definitions

**Structured Code Reviews**
Code reviews where you provide meaningful, educational feedback — not just approvals. Focus on correctness, maintainability, failure modes, and knowledge sharing.

> Example: In a PR review, you flag that a new endpoint lacks input validation and suggest a pattern the team already uses elsewhere. You explain *why* it matters (security, consistency) rather than just requesting a change. A review that is just "LGTM" does not count.

**Mentorship Sessions**
Intentional 1:1 or small-group sessions where you help team members grow. Can be pairing, architecture walkthroughs, career conversations, or debugging sessions.

> Example: You spend 30 minutes pairing with a junior developer on how to design a database migration safely. Or you walk a mid-level engineer through how to evaluate trade-offs between two caching approaches.

**Onboarding Support**
Helping new team members become productive — setting up environments, explaining architecture, reviewing their first PRs with extra context, or creating onboarding documentation.

> Example: A new developer joins and you walk them through the system architecture, point them to key documentation, and assign them a well-scoped starter task. You review their first PR with detailed explanations of team conventions.

---

## 🚀 Strategic Impact

| Indicator | Target | Current |
|---|---|---|
| Cost or Performance Improvements | Monthly | |
| Risks Anticipated | Continuous | |
| Process Improvements | 1 per month | |

### Definitions

**Cost or Performance Improvements**
Measurable improvements to system performance, infrastructure cost, or operational efficiency that you identified and drove.

> Example: You noticed a database query running on every API call was doing a full table scan. You added an index and reduced response time from 800ms to 50ms. Or: You identified unused cloud resources costing $500/month and cleaned them up.

**Risks Anticipated**
Technical or operational risks you identified *before* they became problems. This is the core tech lead superpower — seeing around corners.

> Example: You notice the team is building a feature that assumes a third-party API will always respond in under 200ms. You flag this risk, propose a timeout and fallback strategy, and prevent a future production incident.

**Process Improvements**
Changes to how the team works that improve predictability, quality, or developer experience.

> Example: You propose adding a lightweight PR checklist that reduces back-and-forth in reviews by 30%. Or: You set up automated deploy previews so QA can test PRs without waiting for staging deployments.

---

## 📅 Weekly Summary Template

```text
📦 Delivery:
- Sprint commitment: X%
- X blockers removed

🏗 Quality:
- Refactoring in module X
- Identified risk in Y
- Critical incidents: 0

🤝 Team:
- X code reviews
- X mentorship sessions

🚀 Strategy:
- Proposed improvement in X
- Identified long-term scalability concern
```
