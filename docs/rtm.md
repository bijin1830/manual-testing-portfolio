# Sample Requirement Traceability Matrix (RTM)

The RTM links fictional business requirements to test coverage and helps identify missing or duplicate validation.

| Requirement ID | Requirement | Related test scenarios | Priority | Coverage |
|---|---|---|---|---|
| REQ-001 | Registered user can log in with valid credentials | AUTH-01, AUTH-02, AUTH-03 | High | Covered |
| REQ-002 | User session is terminated on logout | AUTH-05 | High | Covered |
| REQ-003 | Customer can search for products | CART-01, CART-02, CART-03 | Medium | Covered |
| REQ-004 | Cart allows add, remove and quantity update | CART-04, CART-05, CART-06 | High | Covered |
| REQ-005 | Cart totals recalculate when quantity changes | CART-07 | High | Covered |
| REQ-006 | Checkout requires mandatory customer/address data | CHK-01, CHK-02, CHK-03 | High | Covered |
| REQ-007 | Checkout amount must match payment amount | CHK-04, PAY-06 | Critical | Covered |
| REQ-008 | Approved payment creates a single successful order | PAY-01, PAY-05 | Critical | Covered |
| REQ-009 | Declined/cancelled payment must not appear successful | PAY-02, PAY-03 | Critical | Covered |
| REQ-010 | Timeout/retry must not create duplicate order | PAY-04, PAY-05 | Critical | Covered |
| REQ-011 | Successful order is visible in history | ORD-01, ORD-02 | High | Covered |
| REQ-012 | Eligible order supports refund request | REF-01, REF-02, REF-03 | High | Covered |

## How I use an RTM

- Confirm every important requirement has test coverage.
- Trace failed test cases back to business impact.
- Identify scope changes when a requirement is updated.
- Select regression tests based on impacted requirements.
- Support UAT/release-readiness discussions with clear coverage evidence.

A production RTM may also contain test-case IDs, defect IDs, execution status, build number and business sign-off, depending on the project process.
