# Tech Lead Task Planning Template

**Task/Feature Name:** _[Brief descriptive name]_
**Ticket/Issue:** _[Link or ID]_
**Date:** _[YYYY-MM-DD]_
**Tech Lead:** _[Your name]_

---

## 1. Problem Clarification

### What are we solving?
_[Describe the problem in simple, shared language - avoid jargon]_

### What are we NOT solving? (Non-goals)
- _[Be explicit about scope boundaries]_
-

### Definition of Done
_[Clear, testable criteria for completion]_
-
-
-

---

## 2. Solution Approach

### Option A: _[Name]_
**Description:**
_[Brief explanation]_

**Pros:**
-

**Cons:**
-

**Trade-offs:**
_[Key considerations]_

### Option B: _[Name]_ (if applicable)
**Description:**
_[Brief explanation]_

**Pros:**
-

**Cons:**
-

**Trade-offs:**
_[Key considerations]_

### Recommended Approach
_[Which option and why - prioritize simplicity and safety]_

---

## 3. Risk Assessment & De-Risking Plan

Check all that apply and document mitigation:

- [ ] **Legacy code involved**
  _Risk:_
  _Mitigation:_

- [ ] **External dependency** (API, service, library)
  _Risk:_
  _Mitigation:_

- [ ] **Requirements unclear or incomplete**
  _Risk:_
  _Mitigation:_

- [ ] **Data impact** (migration, existing records, compatibility)
  _Risk:_
  _Mitigation:_

- [ ] **Performance or scalability concerns**
  _Risk:_
  _Mitigation:_

- [ ] **Security or validation impact**
  _Risk:_
  _Mitigation:_

- [ ] **Cross-team dependency**
  _Risk:_
  _Mitigation:_

- [ ] **Environment differences** (dev / staging / prod)
  _Risk:_
  _Mitigation:_

- [ ] **Testing gaps or difficult-to-test scenarios**
  _Risk:_
  _Mitigation:_

- [ ] **Deployment / rollback risk**
  _Risk:_
  _Mitigation:_

### Highest Risk Item (Attack First)
_[What's the riskiest part that needs validation/proof early?]_

---

## 4. Work Breakdown & Team Coordination

### Task Breakdown
_[Split work to enable parallel progress]_

1. **Task:** _[Description]_
   **Owner:** _[Name or TBD]_
   **Dependencies:** _[What must be done first]_

2. **Task:** _[Description]_
   **Owner:** _[Name or TBD]_
   **Dependencies:** _[What must be done first]_

3. **Task:** _[Description]_
   **Owner:** _[Name or TBD]_
   **Dependencies:** _[What must be done first]_

### Parallelization Strategy
_[How can team members work independently?]_

---

## 5. Quality & Safety Checklist

### Testing Strategy
- [ ] Unit tests
- [ ] Integration tests
- [ ] Edge cases identified and tested
- [ ] Performance/load testing (if applicable)

### System Health
- [ ] Logging/observability added
- [ ] Error handling defined
- [ ] Failure modes identified
- [ ] Rollback plan documented

### Code Review Focus Areas
_[What should reviewers pay special attention to?]_
-
-

---

## 6. Communication Plan

### Initial Alignment Needed
_[Who needs to be consulted before starting?]_
- [ ] Product/PM: _[What to confirm]_
- [ ] Design: _[What to confirm]_
- [ ] Other teams: _[What to confirm]_
- [ ] Security: _[What to confirm]_

### Update Cadence
- **Daily updates:** _[Where - Jira, Slack, standup]_
- **Blockers escalation:** _[To whom, via what channel]_

### Key Stakeholders
_[Who needs to be kept informed?]_
-

---

## 7. Deployment & Validation

### Deployment Strategy
_[How will this be rolled out?]_
- [ ] Feature flag (if applicable)
- [ ] Gradual rollout plan
- [ ] Rollback procedure documented

### Success Metrics
_[How will we know it's working?]_
-
-

### Monitoring & Validation
_[What to watch post-deployment]_
-
-

---

## 8. Decision Log

_[Document key decisions made during execution]_

| Date | Decision | Rationale | Stakeholders |
|------|----------|-----------|--------------|
| | | | |

---

## 9. Completion Checklist

- [ ] All tests passing
- [ ] Code reviewed and merged
- [ ] Deployed to staging
- [ ] Validated in staging
- [ ] Deployed to production
- [ ] Metrics/monitoring healthy
- [ ] No regressions observed
- [ ] Documentation updated
- [ ] Team notified of completion
- [ ] Manager informed with status

---

## Notes & Learnings

_[Capture insights, gotchas, or things to remember for next time]_
