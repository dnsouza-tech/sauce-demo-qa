# Test Summary Report — Sauce Demo

**Project:** Sauce Demo — Manual QA Evaluation
**Tester:** Douglas Souza
**Test period:** May 2025
**Application:** https://www.saucedemo.com

---

## Executive summary

A manual functional testing cycle was conducted on Sauce Demo, covering the core user flows of an e-commerce application: authentication, product browsing, cart management, and checkout.

Out of 21 test cases executed, 18 passed and 3 failures were identified. All failures have been documented as bug reports with detailed steps to reproduce, severity classification, and business impact assessment.

---

## Results overview

| Flow | Test cases | Passed | Failed |
|---|---|---|---|
| Login / Authentication | 5 | 4 | 1 |
| Product listing and sorting | 6 | 5 | 1 |
| Cart management | 6 | 6 | 0 |
| Checkout | 6 | 5 | 1 |
| **Total** | **21** | **18** | **3** |

---

## Bugs found

| ID | Summary | Severity | Status |
|---|---|---|---|
| BUG001 | Locked user receives generic, unprofessional error message | Medium | Open |
| BUG002 | All product images broken for problem_user | High | Open |
| BUG003 | Checkout form accepts submission with missing required fields | High | Open |

---

## Key observations

**What works well**
- The standard user flow — login, browsing, cart, and checkout — works end to end without critical issues.
- Sorting and filtering function correctly.
- Cart state is preserved across page navigation.

**What needs attention**
- The application has a known problematic user profile (`problem_user`) that simulates UI defects. These defects, if present in a real product, would directly impact conversion rates.
- Form validation on the checkout page is inconsistent and poses a risk to data quality and fulfillment operations.
- Error messaging for blocked users lacks clarity and professionalism, which affects customer trust.

---

## Business impact summary

The two high-severity bugs identified — broken product images and incomplete checkout validation — represent direct risks to revenue and customer retention in a real e-commerce environment. Product images influence purchase decisions; checkout data integrity ensures order fulfillment. Both are critical paths that require immediate attention before any production release.

---

## Recommendation

The application is functional for standard users performing core flows. However, it should not be considered release-ready until BUG002 and BUG003 are resolved, as both carry direct business risk. BUG001, while lower in severity, should also be addressed to maintain a professional user experience.

---

*Report prepared by Douglas Souza — Manual QA*
*[LinkedIn](https://www.linkedin.com/in/dnsouza-tech) · [GitHub](https://github.com/dnsouza-tech)*
