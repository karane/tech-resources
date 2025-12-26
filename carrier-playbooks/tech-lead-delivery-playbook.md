# Tech Lead Delivery Playbook
*A practical, engineer-friendly guide to delivering work that keeps both the system and the manager happy.*

---

## 1. How a Senior / Tech Lead Should Behave When Delivering Tasks

### Core Mindset Shift
As a Tech Lead, you are no longer measured by how fast you code, but by:
- How predictably the team delivers
- How safe the system remains
- How calm and informed the manager feels

Your job is to **remove uncertainty**.

---

### 1. Clarify the Problem (For Everyone)
- Reframe the task in simple, shared language
- Explicitly state non-goals
- Align on a clear definition of done

Example:
> Scope is backend-only validation.  
> No schema changes.  
> Done = invalid requests rejected + tests.

---

### 2. Shape the Solution Early
- Propose 1–2 solution options
- Call out trade-offs
- Choose the simplest safe approach

Example:
> Option A: Local validation (fast, low risk)  
> Option B: Shared library (cleaner, slower)  
> Recommendation: Option A due to timeline

---

### 3. De-Risk First (Senior Superpower)
Identify risks early:
- Legacy code involved?
- External dependency (API, service, library)?
- Requirements unclear or incomplete?
- Data impact (migration, existing records, compatibility)?
- Performance or scalability concerns?
- Security or validation impact?
- Cross-team dependency?
- Environment differences (dev / staging / prod)?
- Testing gaps or difficult-to-test scenarios?
- Deployment / rollback risk?

Action:
- Attack the riskiest part first
- Communicate risks clearly and early

Example:
* > This touches legacy auth code; I’ll validate behavior first.
* > This depends on the Payments API response format. If the contract changed, we may need adjustments — I’ll confirm early.
* > Error-handling behavior isn’t specified. I’ll implement a default and confirm expected behavior with the product team.
* > This query may impact performance under high load. I’ll add basic benchmarks and flag if optimization is needed.
* > Existing records may not follow the new validation rules. I’ll scan current data and report potential conflicts.
* > This change affects input validation. I’ll double-check edge cases to avoid introducing injection risks.
* > Implementation is straightforward, but testing may take longer due to multiple scenarios. I’ll update if timing shifts.
* > This requires confirmation from the frontend team on payload format. I’ll sync with them before finalizing.
* > This logic behaves differently in staging vs production due to config differences. I’ll validate in both environments.
* > Deployment touches a shared component. I’ll prepare a rollback plan in case unexpected behavior appears.
  
---

### 4. Unblock the Team
- Split work so others can move in parallel
- Assign clear ownership
- Avoid duplicated effort

Example:
> I handle architecture and risk areas  
> Dev A implements endpoints  
> Dev B focuses on tests

---

### 5. Control the Delivery Narrative
Managers don’t read code — they read updates.

Your updates should always answer:
- Are we on track?
- What’s risky?
- Do you need help?

---

### 6. Review for System Health
In reviews, prioritize:
- Correctness
- Maintainability
- Failure modes
- Observability

Avoid style wars and personal preferences.

---

### 7. Protect Quality Under Pressure
When deadlines tighten:
- Reduce scope, not safety
- Keep tests, logging, and rollback paths

Never trade system stability for speed.

---

### 8. Close the Loop Explicitly
Never just say “done”.

Example:
> Feature merged, deployed to staging, metrics look healthy, no regressions observed.

---

### 9. Absorb Noise
- Shield the team from churn
- Handle clarification and reprioritization
- Keep engineers focused

This invisible work builds massive trust.

---

### Golden Rules for Tech Leads
- No surprises
- Fewer decisions for your manager
- Fewer risks reaching production
- More clarity for the team

---

## 2. Manager Update Templates (Jira / Slack Optimized)

---

## Daily Tech Lead Update

```text
TL Daily Update – <Project / Epic>

Status: 🟢 On track | 🟡 At risk | 🔴 Blocked

Done:
- 

In Progress:
- 

Next:
- 

Risks / Blockers:
- None

Asks:
- None
```

### Example

```text
TL Daily Update – Payments API Refactor

Status: 🟢 On track

Done:
- Legacy validation risk analyzed
- Spike completed successfully

In Progress:
- API changes in development
- Reviewing test coverage

Next:
- Review PRs
- Confirm rollout plan

Risks / Blockers:
- None

Asks:
- None
```

---

## Weekly Tech Lead Update

```text
TL Weekly Update – <Project / Epic>

Overall Status: 🟢 | 🟡 | 🔴

Highlights:
- 

Delivered:
- 

Planned Next Week:
- 

Risks / Mitigations:
- 

Decisions Needed:
- None
```

### Example

```text
TL Weekly Update – Payments API Refactor

Overall Status: 🟢

Highlights:
- High-risk legacy path removed early
- Team parallelized effectively

Delivered:
- API validation changes
- Unit and integration tests
- Staging deployment

Planned Next Week:
- Production rollout
- Monitoring and cleanup

Risks / Mitigations:
- Low rollout risk; rollback plan ready

Decisions Needed:
- None
```

---

## Ultra-Minimal One-Liners

**Daily**
```text
Payments API: 🟢 on track, legacy risk cleared, PRs in review, no blockers.
```

**Weekly**
```text
Payments API: 🟢 delivered validation + tests; prod rollout next week; no decisions needed.
```

---

## Final Reminder
A calm manager is a signal of a well-led system.

Predictability > heroics  
Clarity > verbosity  
Risk management > speed
