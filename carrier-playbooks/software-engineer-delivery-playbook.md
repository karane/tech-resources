# Software Engineer Delivery Playbook
*A practical, engineer-friendly guide to delivering tasks that keep the system reliable and the manager confident.*

---

## 1. How a Software Engineer Should Approach Task Delivery

### Core Mindset
Your goal is not just to finish tasks, but to:
- Deliver predictably
- Avoid surprises
- Make progress visible
- Protect system quality

Managers trust engineers who are **clear, reliable, and proactive**.

---

### 1. Clarify the Task Before Coding
Before writing code:
- Restate the task in your own words
- Confirm scope (what is in / out)
- **Confirm deadline and priority**
- Confirm definition of done

Example:
> This task adds backend validation only, no UI changes.  
> Done = invalid requests rejected + unit tests.

---

### 2. Identify Risks Early
Think briefly about:
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

If you see a risk:
- Communicate it early
- Don’t wait until the deadline

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

### 3. Break the Task Into Steps
Mentally or in Jira:
- Analysis
- Implementation
- Tests
- Review
- Deployment

This helps with estimation and progress reporting.

---

### 4. Give Realistic Estimates
Avoid best-case estimates.

Best practice:
- Estimate
- Add buffer (20–30%)
- Communicate clearly

Example:
> I expect to finish by Thursday EOD; I’ll flag early if that changes.

---

### 5. Make Progress Visible (Especially Remote)
**Silence creates uncertainty.**

Provide short async updates:
- What’s done
- What’s next
- Any blockers

---

### 6. Write Review-Friendly Code
Focus on:
- Readability
- Small commits
- Clear commit messages
- Simple solutions

---

### 7. Test Like a User
Before saying “done”, check:
- Happy path
- Obvious edge cases
- Error handling
- Logs (when applicable)

---

### 8. Deliver With Context
Don’t just say “done”.

Say:
> Task completed, tests added, PR opened, no breaking changes.

---

### 9. Close the Loop
After merge or deploy:
- Monitor briefly
- Fix small follow-ups quickly
- Stay available

---

### Golden Rules for Engineers
- No surprises
- Communicate early
- Deliver predictably
- Protect quality

---

## 2. Manager Update Templates (Jira / Slack Optimized)

---

## Daily Engineer Update

```text
Daily Update – <Task / Ticket>

Done:
- 

Next:
- 

Blockers:
- None
```

---

### Example

```text
Daily Update – JIRA-4321

Done:
- Backend validation implemented
- Unit tests added

Next:
- Open PR
- Address review feedback

Blockers:
- None
```

---

## Ultra-Minimal Update

```text
JIRA-4321: validation done, tests added; next PR; no blockers.
```

---

## PR Description Template

```text
What:
- 

Why:
- 

Tested:
- 
```

---

## Final Reminder
Managers don’t need constant explanations.
They need clarity, predictability, and early signals.

Do those well, and trust follows.
