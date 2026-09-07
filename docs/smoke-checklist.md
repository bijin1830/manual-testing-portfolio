# Smoke Testing Checklist

A lightweight checklist for confirming that a new build is stable enough for detailed testing.

> All examples are generic and synthetic.

## Build & Environment

- [ ] Correct build/version is installed
- [ ] Application launches without crash
- [ ] Required services are reachable
- [ ] Test environment configuration is correct
- [ ] Login page or landing page loads successfully

## Core Functional Flow

- [ ] Valid user can log in
- [ ] Main navigation works
- [ ] Critical screens open without error
- [ ] Basic create/update/view flow works where applicable
- [ ] Search or lookup works with valid data
- [ ] Mandatory validations are triggered
- [ ] Save/submit action completes successfully
- [ ] User receives a clear success or failure message

## Payment-Critical Smoke Checks

- [ ] Purchase flow can be initiated
- [ ] Approved transaction displays a success result
- [ ] Declined transaction displays the correct failure state
- [ ] Cancel action returns control correctly
- [ ] Transaction reference is generated/displayed where expected
- [ ] Receipt/result screen is available where applicable

## Basic Integration Checks

- [ ] Front end can communicate with the required backend/service
- [ ] API-dependent screen returns data
- [ ] Database-backed data is visible after a successful action
- [ ] No obvious timeout or connection error appears

## Result

- **PASS:** Critical flows are available and detailed testing can continue.
- **FAIL:** A blocker affects a core flow; log the issue and stop or limit further testing as appropriate.
