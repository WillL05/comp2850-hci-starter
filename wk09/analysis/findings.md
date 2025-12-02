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
| Mean errors | 0.7 | 1.0 | 0.8 |
| Mean confidence | 3.5/5 | 3.5/5 | 3.5/5 |

**Interpretation**: High success but errors common - participants accidentaly trying to enter empty data into add task field
(validation). HTMX confidence higher (instant feedback). No-JS participants less sure (PRG redirect, no confirmation message).

---

### Task 3: Edit Task Inline
| Metric | HTMX | No-JS | Overall |
|--------|------|-------|---------|
| Mean time (s) | 28 | 35 | 30.6 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0.7 | 1.0 | 0.8 |
| Mean confidence | 4.7/5 | 3.5/5 | 4.2/5 |

**Interpretation**: High success but errors common (validation). HTMX confidence higher (instant feedback). No-JS participants less sure (PRG redirect, no confirmation message).

---

### Task 4: Completed All Tasks
| Metric | HTMX | No-JS | Overall |
|--------|------|-------|---------|
| Mean time (s) | 28 | 35 | 30.6 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0.7 | 1.0 | 0.8 |
| Mean confidence | 4.7/5 | 3.5/5 | 4.2/5 |

**Interpretation**: High success but errors common (validation). HTMX confidence higher (instant feedback). No-JS participants less sure (PRG redirect, no confirmation message).

---

## Qualitative Themes

### Theme 1: Confirmation Feedback Critical
**Evidence**: 4/5 participants mentioned needing "confirmation it worked"
**Quotes**:
- P1 (HTMX): "I like seeing 'Task added' immediately"
- P3 (No-JS): "I had to scroll down to check it was there - not obvious"

**Design implication**: No-JS path needs explicit success message (PRG currently shows none).

---

### Theme 2: Edit Cancel Button Confusing
**Evidence**: 3/5 participants hesitated on Cancel button
**Quotes**:
- P2: "Will Cancel save my changes or lose them?"
- P4: "I clicked it to test - wasn't sure"

**Design implication**: Button label needs clarification ("Cancel (discard changes)")

---

### Theme 3: Keyboard Access Excellent
**Evidence**: 2 participants tested keyboard-only (requested). Both succeeded all tasks.
**Quotes**:
- P5 (keyboard-only): "Tab order makes sense, focus always visible"

**Design implication**: Keep current keyboard implementation.

---

## Accessibility Observations

### Screen Reader (NVDA)
- ✅ Labels announced correctly ("Task title, edit text")
- ✅ Status messages announced ("Task added successfully")
- ❌ Error messages not announced in no-JS path (redirect loses `role="alert"`)

### Keyboard Navigation
- ✅ All features reachable
- ✅ Focus visible
- ⚠️ Tab order logical but Edit→Save→Cancel could be clearer

---

## Prioritised Issues

Based on frequency + severity:

1. **High**: No confirmation message in no-JS path (affects 2/2 no-JS participants, low confidence)
2. **Medium**: Cancel button ambiguous (3/5 confused, but completed anyway)
3. **Low**: Edit button focus order (minor hesitation, all succeeded)
