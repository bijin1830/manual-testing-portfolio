# Manual Test Scenarios

These scenarios are based on the fictional Customer Commerce Portal described in the README.

## Authentication

| ID | Scenario | Type | Priority |
|---|---|---|---|
| AUTH-01 | Login with valid credentials | Positive | High |
| AUTH-02 | Login with incorrect password | Negative | High |
| AUTH-03 | Submit login with blank mandatory fields | Negative | High |
| AUTH-04 | Verify password is masked | Security/UX | Medium |
| AUTH-05 | Verify session behavior after logout | Functional | High |
| AUTH-06 | Verify account lock/error handling after repeated failures | Negative | Medium |

## Product search and cart

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CART-01 | Search using exact product name | Positive | High |
| CART-02 | Search using partial text | Positive | Medium |
| CART-03 | Search with no matching result | Negative | Medium |
| CART-04 | Add product to cart | Functional | High |
| CART-05 | Update item quantity | Boundary | High |
| CART-06 | Remove item from cart | Functional | High |
| CART-07 | Verify subtotal after quantity change | Data validation | High |
| CART-08 | Verify cart state after navigation | Functional | Medium |

## Checkout

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CHK-01 | Checkout with valid mandatory data | Positive | Critical |
| CHK-02 | Checkout with missing address | Negative | High |
| CHK-03 | Validate maximum field lengths | Boundary | Medium |
| CHK-04 | Verify cart total is unchanged when moving to checkout | Integration | Critical |
| CHK-05 | Verify back navigation does not duplicate order/cart items | Negative | High |

## Payment result handling

| ID | Scenario | Type | Priority |
|---|---|---|---|
| PAY-01 | Approved payment creates one order | Positive | Critical |
| PAY-02 | Declined payment does not create successful order | Negative | Critical |
| PAY-03 | Customer cancels payment | Negative | High |
| PAY-04 | Payment response times out | Negative | Critical |
| PAY-05 | Retry after timeout does not create duplicate order | Integration | Critical |
| PAY-06 | Order total matches amount shown before payment | Data validation | Critical |

## Orders and refunds

| ID | Scenario | Type | Priority |
|---|---|---|---|
| ORD-01 | Successful order appears in order history | Functional | High |
| ORD-02 | Order confirmation shows correct reference and amount | Data validation | High |
| REF-01 | Eligible completed order can request refund | Positive | High |
| REF-02 | Ineligible order cannot request refund | Negative | High |
| REF-03 | Refund status is visible after request | Functional | Medium |

## Cross-cutting checks

- Error messages are clear and relevant.
- Mandatory fields are consistently identified.
- Duplicate actions are prevented where applicable.
- Date/time, currency and amount formats remain consistent.
- Browser refresh/back behavior does not cause duplicate submissions.
- Critical actions provide a clear final state to the user.
