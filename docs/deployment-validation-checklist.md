# Deployment Validation Checklist

A practical checklist for validating an application deployment from a QA/support perspective.

> This reflects deployment verification and troubleshooting support, not DevOps ownership.

## Before Deployment

- [ ] Confirm target environment
- [ ] Confirm expected application/build version
- [ ] Confirm required configuration files/values are available
- [ ] Confirm database/script changes are identified where applicable
- [ ] Confirm rollback or previous-version reference is available
- [ ] Record current service/container status before changes

## Deployment / Service Checks

- [ ] Required services start successfully
- [ ] Docker containers are running where applicable
- [ ] Docker Compose services show the expected state
- [ ] No container/service is repeatedly restarting
- [ ] Required ports are listening/reachable
- [ ] IIS/application pool/site is running where applicable
- [ ] No obvious startup exception appears in logs

## Application Validation

- [ ] Application/UI is accessible
- [ ] Login works
- [ ] Main critical flow works
- [ ] API/service connectivity is available
- [ ] Database connectivity is working
- [ ] Configuration changes are reflected correctly
- [ ] Static files/pages load normally

## Post-Deployment Smoke Test

- [ ] Run critical smoke scenarios
- [ ] Validate one successful core transaction/action
- [ ] Validate one expected negative scenario
- [ ] Verify reporting/history reflects the test action where applicable
- [ ] Confirm logs do not show unexpected critical errors

## Troubleshooting Checks

- [ ] Review container/service logs for errors
- [ ] Check service/container restart status
- [ ] Check port/network connectivity
- [ ] Check environment-specific configuration
- [ ] Check database connection/access
- [ ] Compare behavior with the previous working version if required

## Evidence to Record

- [ ] Deployment date/time
- [ ] Environment
- [ ] Application/build version
- [ ] Service/container status
- [ ] Smoke-test result
- [ ] Sanitized error/log evidence if any issue is found
- [ ] Final deployment validation result: PASS / PASS WITH OBSERVATIONS / FAIL
