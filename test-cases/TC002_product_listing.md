# TC002 — Product Listing and Sorting

**Flow:** Product browsing
**Priority:** Medium
**Tester:** Douglas Souza

---

## TC002-01 — Products page loads correctly

```gherkin
Given the user is logged in as "standard_user"
When the products page loads
Then at least one product should be displayed
And each product should show a name, price, and "Add to cart" button
```

**Result:** Pass

---

## TC002-02 — Sort products by price (low to high)

```gherkin
Given the user is on the products page
When the user selects "Price (low to high)" from the sort dropdown
Then products should be displayed in ascending order by price
```

**Result:** Pass

---

## TC002-03 — Sort products by price (high to low)

```gherkin
Given the user is on the products page
When the user selects "Price (high to low)" from the sort dropdown
Then products should be displayed in descending order by price
```

**Result:** Pass

---

## TC002-04 — Sort products by name (A to Z)

```gherkin
Given the user is on the products page
When the user selects "Name (A to Z)" from the sort dropdown
Then products should be listed in alphabetical order
```

**Result:** Pass

---

## TC002-05 — Product detail page

```gherkin
Given the user is on the products page
When the user clicks on a product name
Then the product detail page should open
And it should display the product name, description, price, and an "Add to cart" button
```

**Result:** Pass

---

## TC002-06 — Product listing with problem_user

```gherkin
Given the user is logged in as "problem_user"
When the products page loads
Then product images should display correctly
```

**Result:** Fail — see BUG002
