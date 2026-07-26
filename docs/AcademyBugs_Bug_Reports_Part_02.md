# Bug Reports — AcademyBugs.com Exploratory Testing (Part 2 of 2)

**Project:** AcademyBugs.com — Exploratory Bug Hunt (Functional, Visual, Content, Performance, Crash)
**Tester:** Azeem Mohamed Husain
**Environment:** Chrome (latest), Desktop
**Date:** July 2026

*This is Part 2 of 2 — covering Functional, Performance, and Crash Bugs, plus the Summary Table. See Part 1 for Content and Visual Bugs.*

---

## Functional Bugs

### FUNCTIONAL-01: Social Share Icons Non-Functional
**Category:** Functional
**Severity:** Low–Medium
**Description:** On the product detail page, social share icons (Facebook, Twitter/X, Email, Pinterest, LinkedIn, MySpace) appear visually grayed out/disabled. Clicking the Twitter/X icon produces no action.
**Steps to Reproduce:**
1. Navigate to any product detail page
2. Click the Twitter/X share icon
**Expected Result:** Clicking should open a share dialog or new tab for sharing the product on Twitter/X.
**Actual Result:** No response to the click.
**Evidence:**

![Screenshot: functional-bug01_twitter-button.png](evidence/functional-bug01_twitter-button.png)

---

### FUNCTIONAL-02: "Manufacturer" Link Leads to Incorrect/Inappropriate Page
**Category:** Functional
**Severity:** Medium
**Description:** On the product detail page, clicking the "Manufacturer: Handmade" link navigates to a page that does not match the expected manufacturer information context.
**Steps to Reproduce:**
1. Navigate to a product detail page
2. Click the "Handmade" manufacturer link
**Expected Result:** Should navigate to a relevant manufacturer information or filtered product page.
**Actual Result:** Navigates to an unrelated/inappropriate page.
**Evidence:**

![Screenshot: functional-bug02_giving_inappropriate_page.png](evidence/functional-bug02_giving_inappropriate_page.png)

---

### FUNCTIONAL-03: Grand Total Calculation Error in Shopping Cart
**Category:** Functional
**Severity:** **High**
**Description:** On the Shopping Cart page, the Grand Total does not match the sum of Cart Subtotal and Shipping.
**Steps to Reproduce:**
1. Add multiple items to cart
2. Navigate to the Shopping Cart page
3. Observe the Cart Totals section (Subtotal, Shipping, Grand Total)
**Expected Result:** Grand Total = Cart Subtotal + Shipping = $559.80 + $7.99 = **$567.79**
**Actual Result:** Grand Total displayed as **$667.79** — a $100.00 discrepancy from the correct calculated value.
**Evidence:**

![Screenshot: functional-bug03_total_balance.png](evidence/functional-bug03_total_balance.png)

**Note:** This is a high-severity, verifiable calculation defect — confirmed independently by recalculating the displayed Subtotal and Shipping values, not just a visual impression.

---

### FUNCTIONAL-04: Price Range Filter Does Not Apply
**Category:** Functional
**Severity:** Medium
**Description:** Selecting a price range filter (e.g., $100.00–$299.99) on the product listing page does not actually filter the displayed products, despite the filter tag appearing as active.
**Steps to Reproduce:**
1. Navigate to the Shop/product listing page
2. Apply a price range filter (e.g., $100–$299.99)
3. Observe the product list and the filter tag
**Expected Result:** Product list should update to show only items within the selected price range.
**Actual Result:** Filter tag shows as applied (with a "(1)" count indicator), but the product list does not actually filter — filter has no effect on displayed results.
**Evidence:**

![Screenshot: functional_bug04_price_range_function.png](evidence/functional_bug04_price_range_function.png)

---

## Performance Bugs

### PERFORMANCE-01: Delay/Unresponsiveness on MySpace Icon Click
**Category:** Performance
**Severity:** Low
**Description:** Clicking the MySpace share icon on the product detail page triggers a noticeable delay/unresponsiveness before any further action can be taken on the page.
**Steps to Reproduce:**
1. Navigate to any product detail page
2. Click the MySpace share icon
3. Observe page responsiveness immediately afterward
**Evidence:**

![Screenshot: performance-bug01_when_click_myspace_icon.png](evidence/performance-bug01_when_click_myspace_icon.png)

---

### PERFORMANCE-02: Billing Address Section Stuck Loading
**Category:** Performance
**Severity:** Medium
**Description:** On the Account page, the Billing Address section displays a persistent loading spinner and does not resolve to show the actual billing address content within a reasonable time.
**Steps to Reproduce:**
1. Log in to an account
2. Navigate to Account > Billing Address section
3. Observe the loading state
**Expected Result:** Billing address details should load and display within a few seconds.
**Actual Result:** Loading spinner persists indefinitely (or for an unreasonably long duration) without resolving.
**Evidence:**

![Screenshot: performance-bug02_billing_address_loading.png](evidence/performance-bug02_billing_address_loading.png)

---

## Crash Bugs

### CRASH-01: Currency Selector Triggers Site Instability
**Category:** Crash
**Severity:** High
**Description:** Interacting with the currency selector (e.g., switching to GBP) triggered the site's crash-detection state, temporarily restricting page access.
**Steps to Reproduce:**
1. Navigate to any page with the currency selector
2. Change currency (e.g., to GBP)
**Actual Result:** Site flagged a crash event; page access was restricted for approximately 5 seconds before becoming usable again.
**Evidence:**

![Screenshot: crash-bug01_search-button.png](evidence/crash-bug01_search-button.png)

---

### CRASH-02: "Retrieve Password" Button Triggers Site Instability
**Category:** Crash
**Severity:** High
**Description:** Clicking "Retrieve Password" on the password recovery form triggered the site's crash-detection state.
**Steps to Reproduce:**
1. Navigate to the Forgot Password page
2. Enter a valid email
3. Click "Retrieve Password"
**Actual Result:** Site flagged a crash event; page was inaccessible for approximately 5 seconds before recovering.
**Evidence:**

![Screenshot: crash-bug02_forget_password.png](evidence/crash-bug02_forget_password.png)

---

### CRASH-03: "Post Comment" Button Triggers Site Instability
**Category:** Crash
**Severity:** High
**Description:** Submitting a comment via the "Post Comment" button on a blog/product comment form triggered the site's crash-detection state.
**Steps to Reproduce:**
1. Fill out the comment form (name, email, website, message)
2. Click "Post Comment"
**Actual Result:** Site flagged a crash event; page was inaccessible for approximately 5 seconds before recovering.
**Evidence:**

![Screenshot: crash-bug04_post_button.png](evidence/crash-bug04_post_button.png)

---

*Note: All three crash bugs share the same observed pattern — a brief (~5 second) full-page lockout immediately after the triggering action, before normal access resumes. This consistent pattern across three different triggers suggests a shared underlying mechanism (e.g., a simulated server error/timeout) rather than three unrelated defects.*

---

## Summary Table

| Category | Bugs Documented | Officially Registered (per site tracker) |
|---|---|---|
| Functional | 4 | 4 |
| Visual | 4 | 3 |
| Content | 5 | 3 |
| Performance | 2 | 3* |
| Crash | 3 | 4* |
| **Total** | **18** | **17** |

*Small discrepancies between documented findings and the tracker's per-category counts are expected — the tracker doesn't always register a submission on the first attempt (a known limitation encountered during this session), and category boundaries for a couple of borderline findings (e.g., loading-related issues) could reasonably sit under either Visual or Performance.

**— End of Part 2. —**
