# QA Portfolio — Sauce Demo

Manual testing project on [Sauce Demo](https://www.saucedemo.com), a demo e-commerce application built for QA practice.

---

## Objective

Validate the core user flows of the application — authentication, product browsing, cart management, and checkout — ensuring functionality, usability, and business impact are properly assessed.

---

## Application under test

- **URL:** https://www.saucedemo.com
- **Type:** E-commerce (demo)
- **Test credentials:**
  - Username: `standard_user`
  - Password: `secret_sauce`

---

## Project structure

```
sauce-demo-qa/
├── README.md
├── TEST_PLAN.md
├── SUMMARY.md
├── test-cases/
│   ├── TC001_login.md
│   ├── TC002_product_listing.md
│   ├── TC003_cart.md
│   └── TC004_checkout.md
└── bug-reports/
    ├── BUG001_locked_user_no_feedback.md
    ├── BUG002_broken_ui_user.md
    └── BUG003_checkout_missing_validation.md
```

---

## Scope

| Flow | Covered |
|---|---|
| Login / Authentication | Yes |
| Product listing and sorting | Yes |
| Cart management | Yes |
| Checkout flow | Yes |
| Logout | Yes |

---

## Test Summary

| Item                | Result                              |
|---------------------|-------------------------------------|
| Test cases          | 4 suites                            |
| Bugs reported       | 4                                   |
| High severity       | 1                                   |
| Medium severity     | 2                                   |
| Techniques applied  | Black Box, Exploratory Test, Error Guessing, Gherkin  |

## Tools used

- **Test management:** Manual (Markdown)
- **Bug tracking:** GitHub Issues + Markdown reports
- **BDD format:** Gherkin (Given/When/Then)
- **Version control:** Git & GitHub

---

## Author

Douglas Souza
[LinkedIn](https://www.linkedin.com/in/dnsouza-tech) · [GitHub](https://github.com/dnsouza-tech)
