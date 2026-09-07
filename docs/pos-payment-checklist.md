# POS Payment Testing Checklist

A practical manual checklist for validating common POS/payment transaction behavior.

> This is a generic, synthetic checklist. It does not contain any real bank, merchant, terminal or production information.

## Terminal Readiness

- [ ] Correct application/build version is installed
- [ ] Terminal is online and configured for the test environment
- [ ] Required parameters are downloaded
- [ ] Date/time is correct
- [ ] Printer is ready where applicable
- [ ] ECR/integration connection is available where applicable

## Purchase

- [ ] Valid purchase is approved
- [ ] Declined purchase shows the expected result
- [ ] Customer cancel is handled correctly
- [ ] Timeout/communication failure behavior is clear
- [ ] Amount displayed on POS matches the requested amount
- [ ] Transaction reference is generated
- [ ] Receipt amount/result matches the transaction

## Card Interface

- [ ] Chip transaction can be initiated
- [ ] Contactless transaction can be initiated
- [ ] Swipe/fallback behavior is handled according to supported flow
- [ ] Unsupported card/application is rejected gracefully
- [ ] Card removal/insertion prompts are clear

## CVM / PIN

- [ ] PIN prompt appears when required
- [ ] Correct PIN can complete the transaction
- [ ] Incorrect PIN returns the expected decline/error
- [ ] Cancel during PIN entry is handled correctly
- [ ] No-PIN flow behaves correctly where permitted

## Refund / Void / Reversal

- [ ] Eligible transaction can be refunded
- [ ] Invalid/excess refund amount is rejected
- [ ] Void works only for eligible transactions
- [ ] Reversal is triggered/recorded when required after an uncertain result
- [ ] Original and follow-up transaction references can be correlated

## Settlement / Totals

- [ ] Batch/settlement can be initiated
- [ ] Successful settlement result is shown
- [ ] No-batch condition is handled correctly
- [ ] Transaction totals match the expected test transactions

## ECR / Integrated Mode

- [ ] Request reaches the POS
- [ ] POS amount matches ECR amount
- [ ] Final POS result is returned to ECR
- [ ] Timeout behavior is handled without duplicate charging
- [ ] Retry/last-transaction flow can be used where supported

## Evidence to Capture

- [ ] Timestamp
- [ ] Transaction type and amount
- [ ] Application/build version
- [ ] Response/error code where available
- [ ] Transaction reference/RRN/STAN using synthetic test data only
- [ ] Relevant sanitized logs/screenshots
