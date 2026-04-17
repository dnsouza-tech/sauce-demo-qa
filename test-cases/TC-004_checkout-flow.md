# TC004 — Checkout Flow

**Flow:** Checkout
**Priority:** High
**Tester:** Douglas Souza

---

## TC004-01 — Initiate checkout

```gherkin
Given the user has at least one item in the cart
When the user clicks "Checkout"
Then the user should be directed to the checkout information form
```

**Result:** Pass

---

## TC004-02 — Complete checkout form with valid data

```gherkin
Given the user is on the checkout information page
When the user enters a valid first name, last name, and postal code
And clicks "Continue"
Then the user should proceed to the order summary page
```

**Result:** Pass

---

## TC004-03 — Submit checkout form with empty fields

```gherkin
Given the user is on the checkout information page
When the user clicks "Continue" without filling in any fields
Then an error message should indicate which fields are required
```

**Result:** Fail — see BUG003

---

## TC004-04 — Review order summary

```gherkin
Given the user has filled in the checkout form
When the order summary page is displayed
Then it should list all cart items with correct names and prices
And show the subtotal, tax, and total amount
```

**Result:** Pass

---

## TC004-05 — Complete purchase

```gherkin
Given the user is on the order summary page
When the user clicks "Finish"
Then a confirmation message should appear
And the cart should be empty
```

**Result:** Pass

---

## TC004-06 — Cancel checkout and return to cart

```gherkin
Given the user is on the checkout information page
When the user clicks "Cancel"
Then the user should be redirected back to the cart page
And all cart items should still be present
```

**Result:** Pass
