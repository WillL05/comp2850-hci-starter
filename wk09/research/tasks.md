# Evaluation Tasks — Week 9
## Task 1: Delete Completed Task
**Scenario**: You've want to see all your COMP2870 worksheets

**Instructions**:
1. Filter by COMP2870
2. Confirm that all COMP2870 worksheets show and allow for deletion and edit

**Success criteria**:
- added COMP2870 tasks show
- doesn't show tasks not comtaining the keyword
- can edit and delete filtered tasks

**Inclusion focus**: keyboard-only editing, Focus management

**Metrics**: 
- 20 seconds
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
**Scenario**: You have made a typo in your task titled COMP2870 worksheet 3

**Instructions**:
1. Find task "COMP2870 worksheet 3"
2. Edit it to say "COMP2860 worksheet 3"
3. save the change

**Success criteria**:
- Edit mode activates (input appears)
- Save updates the title
- Focus returns to edited task

**Inclusion focus**: Focus management, keyboard-only editing, delete button, cancel button

**Metrics**: 
- 35 seconds
- 1
- 0
- HTMX
---

## Task 4: Completed All Tasks
**Scenario**: You have completed all your listed tasks for COMP2870

**Instructions**:
1. Filter by COMP2870
2. Delete all listed tasks
3. No tasks should remain

**Success criteria**:
- added COMP2870 tasks show
- doesn't show tasks not comtaining the keyword
- Task removed from list
- Status message announced
- No tasks remain

**Inclusion focus**: Focus management, keyboard-only editing, delete button, cancel button

**Metrics**: 
- 50 seconds
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

