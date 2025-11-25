# Evaluation Tasks — Week 9

## Task 1: Filter and Complete
**Scenario**: You've just finished your worksheet for the week called worksheet4.

**Instructions**:
1. Find the task titled "worksheet4"
2. Mark it as complete
3. Verify it's marked correctly

**Success criteria**:
- Participant finds correct task within 30 seconds
- Toggle works (checkbox/button responds)
- Visual confirmation shown (strikethrough, badge, status message)

**Inclusion focus**: Keyboard access, screen reader announcement

**Metrics**: 
- 10 seconds
- 1
- 0
- HTMX
---

## Task 2: Add New Task
**Scenario**: You have just been assigned a new worksheet to complete. called worksheet5

**Instructions**:
1. Add a new task: "Submit worksheet5"
2. Confirm it appears in the list

**Success criteria**:
- Form submission works (HTMX + no-JS)
- New task appears immediately (or after reload for no-JS)
- Confirmation message shown

**Inclusion focus**: Error handling (if blank title), status announcements

**Metrics**: 
- 15 seconds
- 1
- 0
- HTMX
---

## Task 3: Edit Task Inline
**Scenario**: You mhave completed all your tasks

**Instructions**:
1. Find all tasks listed
2. delete each one by one
3. should show less tasks each time
4. task list should eventually be empty

**Success criteria**:
- can delete each task one by one
- can easily access multiple tasks to delete them
- task list is empty after all tasks deleted

**Inclusion focus**: Focus management, keyboard-only editing, delete button, screen reader announcement

**Metrics**: 
- 35 seconds
- 1
- 0
- HTMX
---

## Task 4: Delete Completed Task
**Scenario**: You've completed "worksheet 3" and want to remove it.

**Instructions**:
1. Find task "worksheet 3"
2. Delete it
3. Confirm it's gone

**Success criteria**:
- Confirmation shown (HTMX) OR form submits (no-JS)
- Task removed from list
- Status message announced

**Inclusion focus**: Confirmation (HTMX has `hx-confirm`, no-JS has none - documented trade-off)

**Metrics**: 
- 10 seconds
- 1
- 0
- HTMX
---

## Metrics per Task

For each task, record:
- **Time-on-task** (seconds from start to completion)
- **Success** (1 = completed, 0 = abandoned)
- **Error count** (validation errors, wrong clicks)
- **Mode** (HTMX or no-JS)
