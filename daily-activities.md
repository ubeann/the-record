---
type: Project
Status: Active
_icon: anchor
product: APS
---
# Daily Activities

## Today Focus

- [ ] Validate Postman API collection for 3Dolphins integration.
- [ ] Prepare Payment Plan deployment.
- [ ] Continue [[Data Bakcup Management|Data Backup Management]] planning.
- [ ] Generate new SSL certificate for Guestbook.

## Deployment - 12 May 2026

### Scope

| Area     | Changes                                                                                     | Status      | Notes                                         |
| -------- | ------------------------------------------------------------------------------------------- | ----------- | --------------------------------------------- |
| Admin    | Hotfix NPWP and fix publish flagging for Payment Plan, and unit availability adjustment.    | Not started | Confirm release branch and deployment window. |
| Agent    | Fix publish flagging for Payment Plan.                                                      | Not started | Confirm behavior matches Admin.               |
| REST API | Handle reservation cancel issue, Payment Plan adjustment, and unit availability adjustment. | Not started | Validate API response and regression impact.  |

### Pre-Deployment Checklist

- [ ] Confirm final change list with each owner.
- [ ] Ask Mas Rega for production query details.
- [ ] Prepare query and rollback query before execution.
- [ ] Confirm deployment window and affected services.
- [ ] Prepare smoke test checklist for Admin, Agent, and REST API.

### Post-Deployment Validation

- [ ] Verify Admin NPWP hotfix.
- [ ] Verify Payment Plan publish flagging in Admin.
- [ ] Verify Payment Plan publish flagging in Agent.
- [ ] Test reservation cancel flow through REST API.
- [ ] Test Payment Plan adjustment through REST API.
- [ ] Test unit availability behavior after adjustment.
- [ ] Record deployment result and follow-up issues.

## API Validation - 3Dolphins Integration

- [ ] Review Postman collection and environment variables.
- [ ] Validate authentication request.
- [ ] Validate required payload fields.
- [ ] Test success response scenario.
- [ ] Test error response scenarios.
- [ ] Document failed cases, expected behavior, and owner.
- [ ] Share validation result with the integration team.

## Backup And Infrastructure

### Data Bakcup Management

- [ ] Define backup scope.
- [ ] Confirm backup schedule.
- [ ] Confirm retention period.
- [ ] Confirm restore test plan.
- [ ] Identify owner for monitoring and incident response.

### Guestbook SSL

- [ ] Confirm domain and current certificate expiry.
- [ ] Generate new SSL certificate.
- [ ] Install certificate in the target environment.
- [ ] Verify HTTPS access after installation.

## Open Questions

- Who owns each deployment item: Admin, Agent, and REST API?
- What is the approved deployment window for 12 May 2026?
- What production query is required for Payment Plan?
- Is rollback handled by query, redeployment, or both?
