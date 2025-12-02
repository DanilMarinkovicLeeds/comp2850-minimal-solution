# Evaluation Tasks — Week 9

## Task T1: Filter tasks

**Scenario**:
"You've been asked to find all tasks containing '2850'. Use the filter feature to find these tasks and then say how many tasks there are."

**Setup**:
- Pre-populate task list with 10 tasks, 3 containing "2850" in title
- Example: "Finish 2850 backlog", "Complete 2850 job stories", "2850 pilot study", plus 7 others

**Success criteria**:
- Participant uses filter box (types "2850")
- Participant reports correct count (3 tasks)
- Completed within 2 minutes
- Target time 30 seconds
- No validation errors

**Metrics**:
- Time from page load to stating count (ms)
- Completion (0 = fail, 1 = success)
- Validation errors (count)
- Confidence rating (1–5): "How confident are you that you found all matching tasks?"

**Accessibility checks**:
- Result count announced by screen reader?
- Keyboard-only completion possible?
- Works with JS disabled?

---

## Task T2: Edit Task Title

**Scenario**:
"The task 'Complete 2860 quiz by Wednesday' has had its due date change. Change it to 'Complete 2860 quiz by Friday' and save the change."

**Setup**:
- "Complete 2860 quiz by Friday" (visible in list)
- Add other tasks to see how participant navigates task manager.
- Participant must click Edit, change text, save

**Success criteria**:
- Participant activates edit mode
- Participant updates title correctly
- Participant edits correct task
- Change persists after save
- Completed within 90 seconds
- No validation errors
- Target time 30 seconds

**Metrics**:
- Time from click Edit to save confirmation (ms)
- Completion (0/1)
- Validation errors (e.g., blank title submitted by mistake)
- Confidence rating (1–5)

**Accessibility checks**:
- Status message "Updated [title]" announced?
- Focus remains on/near edited task?
- Works with keyboard only?
- Works with JS disabled?

---

## Task T3: Add New Task

**Scenario**:
"You need to remember to 'Submit 2870 worksheet'. Add this as a new task."

**Setup**:
- Partially filled task list with 3 tasks
- Form visible at top of page

**Success criteria**:
- Participant types exact title (or close match)
- Submits form
- New task appears in list
- Completed within 60 seconds
- Target time 30 seconds

**Metrics**:
- Time from focus in input to confirmation (ms)
- Completion (0/1)
- Validation errors (if they submit blank by accident)
- Confidence rating (1–5)

**Accessibility checks**:
- Status message "Added [title]" announced?
- Form remains usable after error (if triggered)?
- Works with JS disabled (PRG)?

---

## Task T4: Filter and Delete Tasks

**Scenario**:
"You have caught up on all of your 2850 work, use the filter to search for all tasks relating to 2850 and delete them"

**Setup**:
- Create at least 8 tasks, 3 of which relate to 2850 and should be deleted.

**Success criteria**:
- Participant clicks Delete button
- Confirms deletion (HTMX path) or submits form (no-JS)
- Task removed from list
- Completed within 150 seconds
- Target time 45 seconds

**Metrics**:
- Time from click Delete to confirmation (ms)
- Completion (0/1)
- Confirmation dialog acknowledged (HTMX only)
- Confidence rating (1–5)

**Accessibility checks**:
- Delete button has accessible name ("Delete task: Test entry")?
- Status message "Deleted [title]" announced (HTMX)?
- Works with keyboard only?
- Works with JS disabled (no confirmation, but functions)?

---

## Task Order

**Recommended sequence**:
1. **Warm-up** (not timed): "Browse the task list and familiarize yourself with the interface."
2. T3 (Add) — Low cognitive load, builds confidence
3. T1 (Filter) — Medium complexity, tests search
4. T2 (Edit) — Tests inline interaction, validation
5. T4 (Filter and delete) — High cognitive load, combines previous task with new task, Destructive action, tests confirmation
6. **Debrief** (qualitative): Open-ended questions

**Counterbalance** if testing multiple participants: alternate T1/T2 order to avoid learning effects.

---

## Notes for Facilitator

- **Do not help** unless participant is completely stuck (>3 min). Note as "facilitated" in observations.
- **Think-aloud optional**: Ask participants to narrate their thoughts if comfortable. Don't force.
- **Screen reader users**: Allow extra time for navigation. Log SR-specific observations separately.
- **Keyboard-only**: Offer keyboard-only variant to 1-2 participants for comparison.
- **No-JS**: Test at least 1 participant with JS disabled to verify parity.

---

## Success Definitions

**Completion codes**:
- `1` = Task fully completed, correct outcome
- `0.5` = Partial completion (e.g., found filter but wrong count)
- `0` = Failed or abandoned

**Time bounds**:
- T1: 120s
- T2: 90s
- T3: 60s
- T4: 150s

If participant exceeds time, prompt: "Would you like to continue, or shall we move to the next task?"
