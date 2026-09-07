# Sample Defect Reports

All examples below are fictional and use synthetic data.

## DEF-001 — Duplicate order created after payment timeout and retry

**Module:** Checkout / Payment  
**Severity:** Critical  
**Priority:** High  
**Environment:** UAT / Demo build 1.0  
**Status:** New

### Preconditions

- User is logged in.
- One item is available in cart.
- Checkout details are valid.

### Steps to reproduce

1. Proceed to checkout.
2. Select the mock payment option.
3. Submit payment.
4. Simulate a delayed/timeout response.
5. Return to checkout and retry the same order.
6. Open Order History.

### Expected result

Only one successful order should exist for the customer action. The application should safely determine the previous transaction state before creating another order.

### Actual result

Two successful orders are displayed with the same amount after the retry.

### Impact

Potential duplicate customer charge/order creation and reconciliation mismatch.

### Evidence to capture

- Timestamp of both attempts
- Order references
- Amount
- Application response/error
- Request correlation/reference if available
- Relevant API/log/database evidence using masked synthetic test data

---

## DEF-002 — Cart total not updated after quantity reduction

**Module:** Cart  
**Severity:** High  
**Priority:** High

### Steps to reproduce

1. Add a product priced at 100.00 to cart.
2. Set quantity to 2.
3. Confirm total shows 200.00.
4. Reduce quantity to 1.

### Expected result

Cart total should update to 100.00.

### Actual result

Quantity changes to 1, but the displayed total remains 200.00 until page refresh.

### Impact

Incorrect amount can be presented to the customer and may affect checkout confidence.

---

## DEF-003 — Logout does not invalidate current browser session

**Module:** Authentication  
**Severity:** High  
**Priority:** Medium

### Steps to reproduce

1. Login with a valid test user.
2. Open the Account page.
3. Click Logout.
4. Use browser Back button.

### Expected result

Authenticated content should not be accessible after logout.

### Actual result

The previously authenticated Account page is displayed and remains interactive.

### QA note

During retest, verify logout from multiple pages and run targeted regression around login, session expiry and protected URLs.

## What I include in a strong defect

- Short, searchable title
- Exact environment/build
- Preconditions
- Numbered reproduction steps
- Expected vs actual behavior
- Severity and priority
- Business/customer impact
- Evidence and identifiers
- Retest notes
