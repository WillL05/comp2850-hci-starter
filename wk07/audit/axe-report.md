# axe DevTools Audit Report — Week 7

**Date**: [2025-11-20]
**Page scanned**: http://localhost:8080/tasks
**axe version**: [e.g., 4.10.3]

---

## Summary

- **Critical**: 1
- **Serious**: 4
- **Moderate**: 0
- **Minor**: 0
- **Total**: 5 issues

---

## Violations Found

### 1. Color Contrast (Serious)
**WCAG**: 1.4.3 Contrast (Minimum) - Level AA
**Issue**: Button text (#6c757d) on white background = 4.2:1 (needs 4.5:1)
**Element**: `<button>Delete</button>` in task list
**Impact**: Low vision, colour-blind people struggle to read
**Fix**: Change button colour to #5a6268 (meets 4.5:1)

--- 

### 2. image alt text (Critical)
**WCAG**: 
**Issue**: Ensure `<img>` elements have alternative text or a role of none or presentation
**Element**: `<img src="/static/img/icon.png" width="16" height="16">`
**Impact**: People using screen readers have no way of translating image into words
**Fix**: Add alt text to image

---

## Needs Review (Manual Check Required)

### 1. Link Purpose (Best Practice)
**WCAG**: 2.4.4 Link Purpose (In Context) - Level A
**Issue**: Link text is "here" (not descriptive)
**Element**: `<a href="/docs">Click here</a>`
**Manual check**: Review if context makes purpose clear
## Passed Checks (Sample)

- ✅ HTML lang attribute
- ✅ Unique IDs
- ✅ Valid ARIA attributes
- ✅ Landmark roles
- ✅ Skip link present

---

## Priority Fixes (Week 7)

Based on severity + inclusion risk:
1. **Missing form labels** (Critical, WCAG A) - FIX NOW
2. **Color contrast** (Serious, WCAG AA) - FIX NOW
3. **Link purpose** (Best practice) - Defer to Week 10
