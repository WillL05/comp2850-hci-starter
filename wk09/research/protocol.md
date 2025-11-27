# Evaluation Protocol — Week 9 Pilots

**Module**: COMP2850 HCI
**Activity**: Task-based usability pilots
**Date**: [2025-11-25]
**Researcher**: [William Lord]

---
**Purpose**: Evaluate usability and accessibility of task list prototype with peer participants.

**Type**: Low-risk formative evaluation, peer-to-peer within module.

**Scope**:
- 3 participants (lab pairs)
- 4 tasks per session (~15–20 minutes)
- No audio/video recording
- No personally identifiable information collected

**Ethical approval**: Covered by module's blanket low-risk consent for peer learning activities (verified with module leader).

**Data retention**: Anonymised logs stored in private repo for academic year, deleted after module assessment complete.

---

## Participant Requirements

**Inclusion**:
- Enrolled in COMP2850
- Comfortable using web browsers
- Able to provide informed consent

**Exclusion**:
- None (module is inclusive by design)

**Accessibility accommodations**:
- Screen reader users: allowed extra time, SR-specific observations recorded separately
- Keyboard-only users: explicitly invited to test no-mouse variant
- No-JS users: at least one session conducted with JS disabled

---

## Consent Process

**Before starting** (read aloud):

> "Thanks for agreeing to pilot our prototype. This is a quick usability test—about 15 minutes. I'll ask you to complete 4 tasks while I observe and take notes. I'm testing the interface, not you, so there are no wrong answers.
>
> **What we're collecting**:
> - Task completion times (from server logs)
> - Whether you complete each task successfully
> - Errors or validation issues
> - Your confidence ratings after each task
> - My notes on any hesitations or accessibility issues
>
> **What we're NOT collecting**:
> - Your name, email, or student ID
> - Screen recordings or audio
> - Your device details beyond 'keyboard-only' or 'screen reader'
>
> I'll assign you a random session code (like `sid=X7kL9p`) which will appear in the logs. You can request that I delete all data linked to your session code at any time, even after today.
>
> **You can stop at any time**, no questions asked, and it won't affect your grade.
>
> Do you have any questions before we start?"

**Verbal consent**: "Are you happy to proceed?"

Record in `wk09/lab-wk9/research/consent-log.md`:


## Purpose

Evaluate task manager usability and accessibility through structured pilots. Data will inform Week 10 redesign and assessment submission.

## Consent (GDPR/Data Protection Act 2018)

**Lawful basis**: Legitimate interest (educational research) + informed consent

**Before starting**, confirm:
- [ ] Purpose explained (evaluate task manager, not testing you)
- [ ] Tasks described (4 scenarios, ~15 minutes)
- [ ] Data collected listed (times, clicks, observations - no PII)
- [ ] Right to withdraw explained (stop anytime, data deleted)
- [ ] Participant verbally consents

**Record**: Participant pseudonym (P1, P2...), date, consent confirmed (initials)

---

## Procedure

### Setup (5 minutes)
1. **Assign mode**: Participant 1 → HTMX, Participant 2 → No-JS (alternate)
2. **Disable JS if needed**: Chrome DevTools → Settings → Disable JavaScript
3. **Set session ID**: Open browser DevTools Console, paste:
   ```javascript
   document.cookie = "sid=P1_7a9f; path=/";  // P1 = Participant 1, random suffix
