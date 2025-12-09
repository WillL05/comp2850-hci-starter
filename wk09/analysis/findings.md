# Pilot Findings Analysis — Week 9

**Participants**: 4 (2 HTMX, 2 No-JS)
**Date range**: [2025-12-01 to 2025-11-01]

---

## Quantitative Summary

### Task 1: Filter and Complete
| Metric | HTMX (n=2) | No-JS (n=2) | Overall |
|--------|------------|-------------|---------|
| Mean time (s) | 11.58 | 20.04 | 15.81 |
| Median time (S) | 11.58 | 20.04 | 14.39 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0 | 0 | 0.0 |
| Mean confidence | 3.5/5 | 3.5/5 | 3.5/5 |

**Interpretation**: Task 1 successful for all. HTMX slightly faster, despite no-JS not requiring page reload. Low error rate. Medium confidence.

---

### Task 2: Add New Task
| Metric | HTMX | No-JS | Overall |
|--------|------|-------|---------|
| Mean time (s) | 10.54 | 15.175 | 12.8575 |
| Median time (S) | 10.54 | 15.175 | 14.605 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0.5 | 0.5 | 0.25 |
| Mean confidence | 3.5/5 | 3.5/5 | 3.5/5 |

**Interpretation**: High success but errors common - participants accidentaly trying to enter empty data into add task field, and being prompted to enter some data and being allowed to enter just spaces into the field - this should not be allowed. And there were complaints about the task added notification not being clear. low error rate. Medium confidence


---

### Task 3: Edit Task Inline
| Metric | HTMX | No-JS | Overall |
|--------|------|-------|---------|
| Mean time (s) | 13.38 | 37.31 | 25.345 |
| Median time (S) | 13.38 | 37.31 | 24.04 |
| Success rate | 100% | 0% | 50% |
| Mean errors | 0.0 | 1.0 | 0.5 |
| Mean confidence | 4.5/5 | 0/5 | 2.25/5 |

**Interpretation**: High success with HTMX but did not work at all with JS-off. Users were not able to edit task at all with JS-off, leading to loss of functionality. Confidence was high in HTMX with users being able to clearly see the filter working and showing correct tasks. JS-off users had no confidence in edit working. Higher error rate. 

---

### Task 4: Completed All Tasks
| Metric | HTMX | No-JS | Overall |
|--------|------|-------|---------|
| Mean time (s) | 16.065 | 30.985 | 23.525 |
| Median time (S) | 16.065 | 30.985 | 19.93 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0.0 | 1.5 | 0.75 |
| Mean confidence | 4.7/5 | 3.5/5 | 4.2/5 |

**Interpretation**: High success but errors common, especially with no-JS as page reload after task deletion makes repetitve deletion annoying for users- requiring them to re-enter filter, subsequently leading to input errors. Confidence higher in HTMX, with no page reload every time. High error rate. High confidence

---

## Qualitative Themes

### Theme 1: Confirmation Feedback Critical
**Evidence**: 2/4 participants mentioned needing "confirmation it worked" 
**Quotes**:
- P1 (HTMX): "I didn't even see the task added sucessfully message at top of page"
- P4 (no-JS): "I wasn't completely sure that the filter was applying "

**Design implication**: Both HTMX and no-JS need better visibility of confirmation in tasks, better highlighting that actions were completed e.g. add, delete and filter .

**WCAG**: 1.4.1 Use of Colour, 4.1.3 Status Messages
**Impact**: 3/5
**Inclusion**:2/5
**Effort**:3/5

**Severity**: Very High

---

### Theme 2: Hard to quickly distinguish between buttons
**Evidence**: 3/4 participants found it difficult to distinguish between the buttons as they are all the same colour
**Quotes**:
- P1: "Confirmation of hovering over the delete button, like an obvious colour, would be nice"
- P2: "the buttons for add and apply filter should be different colours"
- P4: "It was a little hard to see what was selected"

**Design implication**: Button colours for hover and select should be clearer with distinct colours

**WCAG**: 1.4.1 Use of Colour, 3.2.4 Consistent Identification
**Impact**: 2/5
**Inclusion**:3/5
**Effort**:3/5

**Severity**: Very high

---

### Theme 3: Keyboard Access Good
**Evidence**: 2 participants tested keyboard-only (requested). Both succeeded all tasks. However participants found it difficult to see what they had highlighted with the keyboard, making it difficult to keep track of where they were on the page.
**Quotes**:
- P4 (keyboard-only): "was a little hard to see what was selected"

**Design implication**: Keep current keyboard implementation, but change selected colour, making it more visible

**WCAG**: 2.1.1 Keyboard
**Impact**: 3/5
**Inclusion**:5/5
**Effort**:2/5

**Severity**: High

---

### Theme 4: Edit button not working with no-JS

**Evidence**: 2 no-JS participants found that the edit button did not work at all, with the page just reloading on button press 
**Quotes**:
- P2: "Filter didn't work at all
- P4: "I was a little confused with the edit button not working correctly"

**Design implication**: no-JS users could not use the edit button and were unable to make changes to their tasks

**WCAG**: N/A
**Impact**: 4/5
**Inclusion**:3/5
**Effort**:4/5

**Severity**: high


# Redesign Priorities — Week 10 Lab 2

## Priority 1: Make confirmation of actions clearer (MUST FIX)
**Issue**: P1,2 and 4 found it difficult to know whether task had been added to list, P1 didn't even see confirmation message at top of page
**Evidence**: Quotes from participants 
**WCAG**: 1.4.1 Use of Colour, 4.1.3 Status Messages
**Fix**: give text a background of sufficient contrast 
**Effort**: 1 hour

## Priority 2: Distinguishable colours for what is selected
**Issue**: P1 and P4 found it difficult to see what was selected e.g. button or field, especially prevalent on keyboard only 
**Evidence**: quotes
**WCAG**: 1.4.1 Use of Colour, 2.4.7 Focus Indicators
**Fix**: Give hover and select a colour of greater contrast
**Effort**: 1 hour


## Priority 3: Users struggled to distinguish between different buttons and their function (SHOULD FIX)
**Issue**: P1 and P2 had some trouble with quickly identifying the delete and edit buttons, leading to accidentally clicking one or the other
**Evidence**: quotes
**WCAG**: 1.4.1 Use of Colour, 3.2.4 Consistent Identification
**Fix**: Add greater contrast between edit and delete buttons on tasks 
**Effort**: 1 hour

## Deferred (Post-Assessment or Semester 2)
- Edit not working with no-JS
- Filter emotying on task deletion with no-JS
