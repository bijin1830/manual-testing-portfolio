# UAT Readiness Checklist

A sample checklist for deciding whether the fictional Customer Commerce Portal is ready for business/user acceptance testing.

## Before UAT

- [ ] UAT build/version is confirmed.
- [ ] UAT environment is stable and accessible.
- [ ] Required test users and roles exist.
- [ ] Synthetic test data is prepared.
- [ ] Critical integrations/mocks are available.
- [ ] Scope and business scenarios are agreed.
- [ ] Known issues and workarounds are shared.

## Critical business flows

- [ ] User can log in and log out.
- [ ] Product search returns expected results.
- [ ] Cart totals are correct.
- [ ] Checkout mandatory fields are validated.
- [ ] Approved payment creates one order.
- [ ] Declined/cancelled payment is not shown as successful.
- [ ] Timeout/retry does not create duplicates.
- [ ] Order appears in order history with correct details.
- [ ] Refund eligibility rules behave as expected.

## QA evidence

- [ ] Smoke testing passed on the UAT build.
- [ ] Critical functional scenarios passed.
- [ ] Regression testing completed for impacted areas.
- [ ] Open defects are reviewed by severity and business impact.
- [ ] Test execution status is available.
- [ ] Requirement coverage/RTM is updated.

## During UAT

For every business-reported issue, capture:

- Scenario and user role
- Exact timestamp
- Build/environment
- Test data/reference
- Steps performed
- Expected business behavior
- Actual behavior
- Screenshot/log/reference evidence where appropriate

## UAT completion

A UAT completion summary should record:

- Scenarios executed
- Passed/failed/blocked count
- Open defects accepted for release
- Deferred scope
- Business sign-off/status
- Release recommendation or conditions

UAT sign-off is a business decision supported by QA evidence; QA should communicate the remaining product risk clearly rather than only reporting a pass percentage.
