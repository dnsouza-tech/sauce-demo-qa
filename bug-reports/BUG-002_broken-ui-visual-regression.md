# BUG002 — Broken product images for problem_user

**ID:** BUG002
**Related test case:** TC002-06
**Date:** 2025-05-01
**Tester:** Douglas Souza
**Status:** Open

---

## Summary

When logged in as `problem_user`, all product images on the listing page are broken — every product displays the same incorrect image, unrelated to the actual product.

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
3. Observe the product listing page

---

## Expected result

Each product should display its own correct image.

---

## Actual result

All products display the same image, which does not correspond to the products listed. The images are visually identical and clearly incorrect.

---

## Severity

**High**

---

## Business impact

Product images are one of the most critical elements in e-commerce conversion. Research consistently shows that incorrect or missing images significantly reduce purchase intent and increase bounce rate. In a real environment, this type of bug could directly impact revenue and brand perception — customers may lose confidence in the platform and abandon their sessions before purchasing.

---

## Evidence

> Screenshot to be attached.

---

## Suggested fix

Investigate the image mapping logic for different user sessions. Ensure each product's image reference is independent of user profile and correctly linked to its corresponding product ID.
