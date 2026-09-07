# Basic API Validation Checklist

A simple Postman-oriented checklist for manual API validation.

> This reflects basic API testing and validation, not advanced automation or framework development.

## Request Setup

- [ ] Correct HTTP method is used
- [ ] Endpoint/URL is correct for the test environment
- [ ] Required headers are present
- [ ] Authentication/token is valid where required
- [ ] Request body uses the expected format
- [ ] Mandatory fields are included

## Positive Validation

- [ ] Valid request returns the expected HTTP status
- [ ] Response body is returned in the expected format
- [ ] Important response fields are present
- [ ] Returned values match the submitted request where applicable
- [ ] Response message/result is understandable
- [ ] Data is created/updated/retrieved as expected

## Negative Validation

- [ ] Missing mandatory field is rejected correctly
- [ ] Invalid field value returns an appropriate error
- [ ] Invalid authentication is rejected
- [ ] Invalid resource/reference is handled correctly
- [ ] Wrong HTTP method is handled appropriately
- [ ] Empty or malformed request does not cause an unhandled server error

## Basic Response Checks

- [ ] HTTP status code is reasonable for the result
- [ ] Response time is noted if unusually slow
- [ ] JSON/XML structure is valid where applicable
- [ ] Error response contains a useful message/code
- [ ] Sensitive data is not unnecessarily exposed in the response

## Data Validation

- [ ] API result matches the corresponding UI result where applicable
- [ ] Basic SQL/database verification is performed when access is available
- [ ] Duplicate request behavior is checked for important operations
- [ ] Created/updated records contain the expected values

## Evidence to Capture

- [ ] Request method and endpoint
- [ ] Sanitized request body/headers
- [ ] HTTP status
- [ ] Sanitized response
- [ ] Timestamp
- [ ] Environment/build/version where relevant
