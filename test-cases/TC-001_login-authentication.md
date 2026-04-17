# TC001 — Login / Authentication

**Flow:** Authentication
**Priority:** High
**Tester:** Douglas Souza

---

## TC001-01 — Successful login with valid credentials

```gherkin
Given the user is on the login page at https://www.saucedemo.com
When the user enters username "standard_user"
And the user enters password "secret_sauce"
And the user clicks the "Login" button
Then the user should be redirected to the products page
And the page title should display "Products"
```

**Result:** Pass

---

## TC001-02 — Login attempt with invalid credentials

```gherkin
Given the user is on the login page
When the user enters username "standard_user"
And the user enters an incorrect password
And the user clicks the "Login" button
Then an error message should be displayed
And the user should remain on the login page
```

**Result:** Pass

---

## TC001-03 — Login attempt with empty fields

```gherkin
Given the user is on the login page
When the user clicks the "Login" button without entering any credentials
Then an error message should indicate that the username is required
```

**Result:** Pass

---

## TC001-04 — Login with locked user

```gherkin
Given the user is on the login page
When the user enters username "locked_out_user"
And the user enters password "secret_sauce"
And the user clicks the "Login" button
Then an error message should inform the user that their account is locked
```

**Result:** Fail — see BUG001

---

## TC001-05 — Logout

```gherkin
Given the user is logged in as "standard_user"
When the user opens the side menu
And clicks "Logout"
Then the user should be redirected to the login page
And should not be able to access protected pages without logging in again
```

**Result:** Pass
