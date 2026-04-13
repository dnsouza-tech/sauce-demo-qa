# Test Plan — Sauce Demo

## 1. Overview

This document outlines the test strategy and scope for the manual QA evaluation of Sauce Demo, a demo e-commerce application.

---

## 2. Objectives

- Validate that core user flows work as expected
- Identify defects that could impact the user experience or business outcomes
- Assess the application's behavior under different user profiles

---

## 3. Scope

### In scope
- Login and authentication flows
- Product listing, filtering, and sorting
- Cart: adding, removing, and reviewing items
- Checkout: form validation, order summary, and confirmation

### Out of scope
- Performance testing
- Security testing
- Mobile responsiveness
- Automated testing

---

## 4. Test environment

| Item | Details |
|---|---|
| Application URL | https://www.saucedemo.com |
| Browser | Google Chrome (latest) |
| OS | Windows 10 / macOS |
| Test type | Manual — functional |

---

## 5. Test credentials

| Username | Profile |
|---|---|
| `standard_user` | Default user — full access |
| `locked_out_user` | Blocked user |
| `problem_user` | UI issues user |
| `performance_glitch_user` | Slow performance user |

---

## 6. Test cases overview

| ID | Flow | Priority |
|---|---|---|
| TC001 | Login / Authentication | High |
| TC002 | Product listing and sorting | Medium |
| TC003 | Cart management | High |
| TC004 | Checkout flow | High |

---

## 7. Entry and exit criteria

**Entry criteria**
- Application is accessible
- Test credentials are valid
- Test cases are written and reviewed

**Exit criteria**
- All high-priority test cases executed
- All critical and high bugs reported
- Test summary report delivered

---

## 8. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Demo app intentionally has bugs | Medium | Document as known behavior when applicable |
| No backend access | Low | Focus on front-end and UX validation |

---

## 9. Deliverables

- Test cases (Gherkin format)
- Bug reports (with business impact)
- Test summary report
