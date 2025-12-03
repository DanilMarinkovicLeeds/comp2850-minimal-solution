# Peer Pilot Protocol — Week 9

## Study Overview

**Purpose**: Test usability and accessibility of task manager prototype with peer participants to gather feedback that would inform future changes that improve user experience.

**Type**: Low-risk formative evaluation, peer-to-peer within module.

**Scope**:
- 4 participants (lab pairs)
- 4 tasks per session (~5–15 minutes)
- No audio/video recording
- No personally identifiable information collected

**Ethical approval**: Covered by module's blanket low-risk consent for peer learning activities (verified with module leader).

**Data retention**: Anonymised logs stored in private repo for academic year, deleted after module assessment complete.

---

## Participant Requirements

**Inclusion**:
- Enrolled in COMP2850
- Comfortable using web browsers
- Comfortable navigating site with different restrictions (noJS, keyboard only, screen reader)
- Able to provide informed consent

**Exclusion**:
- None

**Accessibility accommodations**:
- Screen reader users: allowed extra time, SR-specific observations recorded separately
- Keyboard-only users: explicitly invited to test no-mouse variant
- No-JS users: at least one session conducted with JS disabled

---

## Consent Process

**Before starting** (read aloud):

> "Thanks for agreeing to pilot our application. This is a quick test that should take around 10 minutes. I'll ask you to complete 4 tasks while I observe and time while taking notes, after I will ask you some questions about your experience. I'm testing the interface, not you, so there are no wrong answers.
>
> **What we're collecting**:
> - Task completion times (from server logs)
> - Whether you complete each task successfully
> - Errors or validation issues
> - Your confidence ratings after each task
> - My notes on any hesitations or accessibility issues
> - Your thoughts on what features were most helpful and which you found most confusing.
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

Record in `wk09/lab-wk9/research/pilot-notes.md`:

**Opt-out path**: If participant requests deletion:
1. Open `data/metrics.csv`
2. Delete all rows where `session_id=X7kL9p`
3. Note in `pilot-notes.md`: "Data deleted on request [date]"

---

## Session Setup

**Environment**:
- Quiet space in lab (not open-plan area)
- Participant laptop/desktop with browser open to prototype
- Facilitator laptop for notes (don't share screen)

**Pre-pilot**:
1. Prepare task manager by adding example tasks
2. Generate random session ID suffix: `openssl rand -hex 3` → e.g., `7a9f2c`
3. Set cookie in participant browser (DevTools Console) using format **P{N}_{random}**:
   ```javascript
   document.cookie = "sid=P1_7a9f; path=/";  // P1 = Participant 1, use P2, P3... for subsequent pilots
