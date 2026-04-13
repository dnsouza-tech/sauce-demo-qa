# BUG003 — Checkout form accepts submission with missing required fields

**ID:** BUG003
**Related test case:** TC004-03
**Date:** 2025-05-01
**Tester:** Douglas Souza
**Status:** Open

---

## Summary

On the checkout information page, it is possible to submit the form without filling in all required fields. The validation does not trigger correctly in all scenarios, allowing incomplete orders to proceed.

---

## Environment

| Item | Details |
|---|---|
| URL | https://www.saucedemo.com/checkout-step-one.html |
| Browser | Chrome 124 |
| OS | Windows 10 |
| User | standard_user |

---

## Steps to reproduce

1. Log in as `standard_user`
2. Add any product to the cart
3. Click "Checkout"
4. Leave the "Last Name" field empty
5. Fill in "First Name" and "Postal Code"
6. Click "Continue"

---

## Expected result

An error message should appear indicating that "Last Name" is a required field and the form should not proceed.

---

## Actual result

The form proceeds to the order summary page without validating the "Last Name" field. The checkout can be completed with incomplete customer information.

---

## Severity

**High**

---

## Business impact

Incomplete customer data collected during checkout creates downstream operational problems: failed deliveries, inability to contact the customer, and issues with order fulfillment. In a real scenario, this type of defect could generate financial losses, logistics failures, and damage to the post-purchase customer relationship — directly affecting retention and satisfaction metrics.

---

## Evidence

> Screenshot to be attached.

---

## Suggested fix

Implement consistent required-field validation on all checkout form fields before allowing the user to proceed. Ensure the validation is triggered on form submission and clearly highlights the missing field to the user.
