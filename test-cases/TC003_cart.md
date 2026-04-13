# TC003 — Cart Management

**Flow:** Shopping cart
**Priority:** High
**Tester:** Douglas Souza

---

## TC003-01 — Add a product to the cart

```gherkin
Given the user is logged in and on the products page
When the user clicks "Add to cart" on any product
Then the cart icon should update to show 1 item
And the button should change to "Remove"
```

**Result:** Pass

---

## TC003-02 — Add multiple products to the cart

```gherkin
Given the user is on the products page
When the user adds 3 different products to the cart
Then the cart icon should display the number 3
```

**Result:** Pass

---

## TC003-03 — Remove a product from the cart (products page)

```gherkin
Given the user has added a product to the cart
When the user clicks "Remove" on that product
Then the product should be removed from the cart
And the cart count should decrease by 1
```

**Result:** Pass

---

## TC003-04 — View cart contents

```gherkin
Given the user has added products to the cart
When the user clicks the cart icon
Then the cart page should display all added products
And each item should show its name, quantity, and price
```

**Result:** Pass

---

## TC003-05 — Remove a product from the cart page

```gherkin
Given the user is on the cart page with at least one item
When the user clicks "Remove" on an item
Then that item should be removed from the cart
```

**Result:** Pass

---

## TC003-06 — Continue shopping from cart

```gherkin
Given the user is on the cart page
When the user clicks "Continue Shopping"
Then the user should be redirected back to the products page
And previously added cart items should still be present
```

**Result:** Pass
