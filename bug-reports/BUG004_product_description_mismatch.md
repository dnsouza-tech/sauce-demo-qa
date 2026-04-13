# BUG004 — Product detail page shows incorrect description for problem_user

**ID:** BUG004
**Related test case:** Exploratory testing
**Date:** 2025-05-01
**Tester:** Douglas Souza
**Status:** Open

---

## Summary

When logged in as `problem_user`, the product detail page displays 
a description that does not match the selected product.

---

## Environment

| Item | Details |
|---|---|
| URL | https://www.saucedemo.com |
| Browser | Chrome 124 |
| OS | Windows 10 |
| User | problem_user |

---

## Steps to reproduce

1. Go to https://www.saucedemo.com
2. Log in with username: `problem_user` and password: `secret_sauce`
3. Click on any product name on the listing page
4. Observe the product name and description on the detail page

---

## Expected result

The product detail page should display the correct name and 
description matching the selected product.

---

## Actual result

The description shown on the detail page does not correspond 
to the selected product, displaying information from a 
different item.

---

## Severity

**High**

---

## Business impact

Incorrect product descriptions on the detail page directly 
affect the user's purchase decision. A customer who reads 
the wrong description may buy the wrong product — leading 
to returns, complaints, and loss of trust in the platform. 
In a real e-commerce environment, this type of defect has 
direct impact on revenue and customer satisfaction metrics.

---

## Evidence

> Screenshot to be attached.

---

## Suggested fix

Investigate the product data binding logic for the 
problem_user session. Ensure each product detail page 
correctly loads its own data independently of user profile.
