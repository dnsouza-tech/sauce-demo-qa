# BUG001 — Locked user receives generic error message

**ID:** BUG001
**Related test case:** TC001-04
**Date:** 2025-05-01
**Tester:** Douglas Souza
**Status:** Open

---

## Summary

When a locked user attempts to log in, the error message displayed is generic and does not clearly inform the user that their account has been specifically blocked.

---

## Environment

| Item | Details |
|---|---|
| URL | https://www.saucedemo.com |
| Browser | Chrome 124 |
| OS | Windows 10 |
| User | locked_out_user |

---

## Steps to reproduce

1. Go to https://www.saucedemo.com
2. Enter username: `locked_out_user`
3. Enter password: `secret_sauce`
4. Click the "Login" button

---

## Expected result

A clear message informing the user that their account has been locked and providing guidance on next steps (e.g., contact support).

---

## Actual result

The message displayed is:
> "Epic saddle bag! This user has been locked out."

The message is informal, unprofessional, and does not provide the user with any actionable guidance.

---

## Severity

**Medium**

---

## Business impact

In a real product, this behavior directly affects customer experience. A user who is blocked — whether for security reasons or inactivity — receives no clear explanation and no path forward. This can lead to frustration, loss of trust, and unnecessary support tickets, increasing operational cost and reducing customer retention.

---

## Evidence

> Screenshot or screen recording to be attached.

---

## Suggested fix

Replace the error message with a professional and informative one, such as:
> "Your account has been locked. Please contact our support team to restore access."
