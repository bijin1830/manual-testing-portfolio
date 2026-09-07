# Sample Test Plan — Customer Commerce Portal

## 1. Objective

Validate that the fictional Customer Commerce Portal supports the critical customer journey reliably from login through checkout, payment result and order history.

## 2. In scope

- Login and session handling
- Product search
- Cart operations
- Checkout validation
- Payment result handling
- Order confirmation and order history
- Refund-request eligibility
- Smoke, functional and regression validation

## 3. Out of scope

- Real bank/scheme connectivity
- Performance/load testing
- Penetration testing
- Production card data
- Third-party systems not represented by the demo requirements

## 4. Test types

| Test type | Purpose |
|---|---|
| Smoke | Confirm critical functions are available on a new build |
| Functional | Validate each requirement and business rule |
| Negative | Validate errors, invalid inputs and failure paths |
| Boundary | Validate minimum/maximum values and limits |
| Integration | Validate hand-off between checkout, payment result and order creation |
| Regression | Confirm existing critical functionality after changes/fixes |
| UAT support | Confirm business-critical scenarios are ready for user acceptance |

## 5. Entry criteria

- Testable build is deployed
- Required test environment is accessible
- Critical requirements are available
- Test accounts/data are prepared
- Known blockers are communicated

## 6. Exit criteria

- All critical scenarios executed
- No open blocker/critical defects affecting release scope
- High-severity defects are reviewed and accepted/fixed
- Failed test cases are documented
- Regression of impacted areas is complete
- UAT readiness status is communicated

## 7. Test data

Synthetic data only:

- Valid and invalid user accounts
- Products with different prices/stock states
- Valid/invalid address values
- Mock payment outcomes: approved, declined, cancelled and timeout
- Eligible and ineligible refund orders

## 8. Risks

| Risk | QA response |
|---|---|
| Requirement ambiguity | Raise questions before execution and record assumptions |
| Environment instability | Separate environment failures from application defects |
| Payment callback delay | Validate duplicate protection and final order state |
| Fix in shared component | Run targeted regression across dependent modules |
| Limited test time | Prioritize critical customer paths and high-risk changes |

## 9. Defect workflow

```text
New → Triaged → Assigned → Fixed → Ready for Retest → Retested → Closed
                                  ↘ Reopened (if issue remains)
```

Severity and priority are assessed separately: severity reflects impact; priority reflects urgency/business need.
