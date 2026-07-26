# Bug Reports — AcademyBugs.com Exploratory Testing (Part 1 of 2)

**Project:** AcademyBugs.com — Exploratory Bug Hunt (Functional, Visual, Content, Performance, Crash)
**Tester:** Azeem Mohamed Husain
**Environment:** Chrome (latest), Desktop
**Testing Approach:** Unscripted exploratory testing guided by Nielsen's Usability Heuristics + general QA error-guessing techniques
**Date:** July 2026

_This is Part 1 of 2 — covering Content Bugs and Visual Bugs. See Part 2 for Functional, Performance, and Crash Bugs plus the Summary Table._

---

## Content Bugs

### CONTENT-01: Garbled Text in Shopping Cart Hover Dropdown

**Category:** Content
**Severity:** Medium
**Description:** In the shopping cart hover/mini-cart dropdown, the line item for "DNK Yellow Shoes" displays unexpected garbled text (`xz2@#`) between the product name and price, where a size/color/variant label would normally appear.
**Steps to Reproduce:**

1. Add "DNK Yellow Shoes" to the cart
2. Hover over the Shopping Cart icon to open the mini-cart dropdown
3. Observe the line item text between the product name and price
   **Expected Result:** The line item should show a meaningful variant label (e.g., color/size) or nothing at all — not placeholder/garbled text.
   **Actual Result:** Displays `xz2@#` — clearly unintended placeholder or corrupted string.
   **Evidence:**

![Screenshot: content-04_shopping_cart_hover.png](evidence/content-04_shopping_cart_hover.png)

---

### CONTENT-02: Malformed Button Text ("RETURN TO STOR E")

**Category:** Content
**Severity:** Low
**Description:** On the empty cart page, the "Return to Store" button renders with a broken word — "RETURN TO STOR" then a large gap, then "E" — suggesting a text/CSS rendering issue splitting the word "STORE."
**Steps to Reproduce:**

1. Remove all items from the cart (or visit the cart page while empty)
2. Navigate to the Shopping Cart page
3. Observe the "Return to Store" button label
   **Expected Result:** Button should read "RETURN TO STORE" as one continuous label.
   **Actual Result:** Text renders broken across the button with irregular spacing.
   **Evidence:**

![Screenshot: content-bug01_button.png](evidence/content-bug01_button.png)

---

### CONTENT-03: Lorem Ipsum Placeholder Text in Product Description

**Category:** Content
**Severity:** Medium
**Description:** The product description section (e.g., on the Silver Heart Bracelet product page) displays generic Lorem Ipsum placeholder text ("Nam nec tellus a odio tincidunt auctor...") instead of an actual product description.
**Steps to Reproduce:**

1. Navigate to a product detail page (e.g., Silver Heart Bracelet)
2. Scroll to the Description section
3. Read the displayed description text
   **Expected Result:** A real, product-specific description should be shown.
   **Actual Result:** Placeholder/dummy text left in what appears to be production content.
   **Evidence:**

![Screenshot: content-bug02.png](evidence/content-bug02.png)

---

### CONTENT-04: Untranslated Foreign-Language Text in "New User" Section

**Category:** Content
**Severity:** Medium
**Description:** In the "New User" section of the sign-in page, a link displays Russian text ("Не зарегистрированы? Нажмите кнопку ниже") instead of English, inconsistent with the rest of the page's language.
**Steps to Reproduce:**

1. Navigate to the Sign In page
2. Look at the "New User" section
3. Observe the link text displayed above "No account? Create an account..."
   **Expected Result:** All visible text should be in English, consistent with the rest of the site.
   **Actual Result:** One link renders in Russian, breaking language consistency.
   **Evidence:**

![Screenshot: content-bug03_new_user.png](evidence/content-bug03_new_user.png)

---

### CONTENT-05: Spelling Error in Color Option ("Yelow")

**Category:** Content
**Severity:** Low
**Description:** On a product page's color selector, the selected color label reads "Yelow" instead of "Yellow."
**Steps to Reproduce:**

1. Navigate to a product detail page with color options
2. Select the yellow color swatch
3. Observe the "Select Color" label text next to the swatch
   **Expected Result:** Color name should be spelled correctly.
   **Actual Result:** Missing letter — "Yelow" instead of "Yellow."
   **Evidence:**

![Screenshot: content-bug04_typo.png](evidence/content-bug04_typo.png)

---

_Note: Per the site's tracker, only 3 of these 5 content findings registered as officially "found" — 2 encountered submission issues during logging, but are documented here regardless since they are genuine, reproducible content defects._

---

## Visual Bugs

### VISUAL-01: Loading Spinner/Text Overlapping Site Logo

**Category:** Visual
**Severity:** Low
**Description:** During page load, the "Please wait…" text and loading spinner render overlapping the "AcademyBugs.com" site logo/header, rather than appearing in a dedicated loading area.
**Steps to Reproduce:**

1. Navigate to any page on the site, or refresh the current page
2. Observe the page during the loading state, before content fully renders
   **Expected Result:** Loading indicator should not visually collide with the site header/logo.
   **Actual Result:** Spinner and text overlap directly onto the logo area.
   **Evidence:**

![Screenshot: visual-bug01.png](evidence/visual-bug01.png)

---

### VISUAL-02: Inconsistent Spacing/Alignment on Product Card

**Category:** Visual
**Severity:** Low
**Description:** On the product detail page, spacing and alignment around the Add to Cart control, price, and stock count appear visually inconsistent compared to other product pages.
**Steps to Reproduce:**

1. Navigate to a product detail page (e.g., Silver Heart Bracelet)
2. Observe the spacing/alignment around the Add to Cart control, price, and stock count
3. Compare with the layout of other product pages
   **Expected Result:** Consistent spacing/alignment should be applied across all product detail pages.
   **Actual Result:** Visual inconsistency observed in this product card's layout.
   **Evidence:**

![Screenshot: visual-bug02_product_card.png](evidence/visual-bug02_product_card.png)

---

### VISUAL-03: Search Box Overlapping Footer Logo on Sign-In Page

**Category:** Visual
**Severity:** Medium
**Description:** On the sign-in page, a "Search" input box renders overlapping the "Test Academy" footer logo/branding area, rather than in its intended position.
**Steps to Reproduce:**

1. Navigate to the Sign In page
2. Scroll down to the footer area
3. Observe the Search box position relative to the "Test Academy" logo
   **Expected Result:** Search box should render in its own clear space without overlapping other page elements.
   **Actual Result:** Search box visually collides with the footer logo.
   **Evidence:**

![Screenshot: visual-bug03_sign_in_button.png](evidence/visual-bug03_sign_in_button.png)

---

### VISUAL-04: Password Label Misalignment

**Category:** Visual
**Severity:** Low
**Description:** On the sign-in page, the "Password\*" label is not properly aligned above its corresponding input field — it appears shifted, creating a visual gap/misalignment relative to the Email field's label-input pairing above it.
**Steps to Reproduce:**

1. Navigate to the Sign In page
2. Observe the Password field label relative to its input box
3. Compare its alignment with the Email field's label-input pairing above it
   **Expected Result:** Password label should align consistently with its input field, matching the Email field's layout pattern.
   **Actual Result:** Label appears offset from its input field.
   **Evidence:**

![Screenshot: visual-bug04_password_alignment.png](evidence/visual-bug04_password_alignment.png)

---

_Note: 3 of these 4 visual findings registered as officially "found" per the site's tracker; documented here in full regardless._

**— End of Part 1. Continue to Part 2 for Functional, Performance, and Crash Bugs. —**
