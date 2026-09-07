# Regression Testing Checklist

This checklist is designed for a typical release after bug fixes or feature changes in the fictional Customer Commerce Portal.

## Build and environment

- [ ] Correct build/version is deployed.
- [ ] Application is reachable.
- [ ] Test accounts and synthetic data are available.
- [ ] Critical external/mock dependencies are reachable.
- [ ] Known environment issues are documented separately from product defects.

## Authentication

- [ ] Valid login works.
- [ ] Invalid login is rejected with correct message.
- [ ] Mandatory-field validation works.
- [ ] Logout invalidates the session.
- [ ] Protected pages are not accessible after logout.

## Search and cart

- [ ] Exact and partial search work.
- [ ] No-result state is handled correctly.
- [ ] Add to cart works.
- [ ] Remove from cart works.
- [ ] Quantity update recalculates totals correctly.
- [ ] Cart data remains consistent when navigating between pages.

## Checkout

- [ ] Mandatory checkout fields are enforced.
- [ ] Amount and item totals match the cart.
- [ ] Back/refresh actions do not duplicate submissions.
- [ ] Checkout can be completed with valid input.

## Payment result handling

- [ ] Approved result creates one successful order.
- [ ] Declined result does not show success.
- [ ] Customer cancel is handled correctly.
- [ ] Timeout has a clear final/recoverable state.
- [ ] Retry after timeout does not create a duplicate order.
- [ ] Payment amount matches order amount.

## Orders and refunds

- [ ] Successful order appears in Order History.
- [ ] Order reference, amount and status are correct.
- [ ] Eligible refund flow is available.
- [ ] Ineligible refund is blocked correctly.
- [ ] Refund status is updated after request.

## Fix-specific regression

For every defect fix:

1. Retest the exact reported steps.
2. Test nearby positive and negative paths.
3. Identify shared components affected by the code change.
4. Run critical end-to-end flows that depend on that component.
5. Confirm no new UI/data inconsistency was introduced.

## Release recommendation

Regression completion should clearly state:

- Total scenarios executed
- Pass/fail/block count
- Open critical/high defects
- Known limitations
- Areas not tested and reason
- QA recommendation for UAT/release
