# Product Scope

## Product Summary

SafetyOps is a multi-tenant Safety Management System for organizations that need a structured way to report safety events, assess risk, track corrective actions, and maintain an auditable record of safety decisions.

The product is SMS-inspired, not a certified compliance product.

## MVP Problem Statement

Small organizations often track safety issues through email, spreadsheets, and disconnected documents. This causes weak visibility, inconsistent risk assessment, missed corrective actions, and poor auditability.

SafetyOps provides one workflow-driven system for safety reports, risk classification, corrective actions, and management visibility.

## MVP Users

### Reporter

Submits hazards, near misses, and incidents.

MVP permissions:

- Create safety reports.
- View reports they submitted.
- View published safety dashboard summaries only if allowed.

### Safety Manager

Owns the safety workflow.

MVP permissions:

- View all reports in tenant.
- Triage reports.
- Update report status.
- Create and assign corrective actions.
- Verify CAPA closure.
- View dashboard and audit timeline.

### Action Owner

Completes assigned CAPA work.

MVP permissions:

- View assigned corrective actions.
- Update CAPA progress.
- Mark CAPA as completed.
- Add completion notes.

### Admin

Manages the organization.

MVP permissions:

- Manage users and roles.
- View all tenant data.
- Configure departments and locations in later phases.

### Viewer

Reads reports and dashboards.

MVP permissions:

- Read-only access to authorized data.

## MVP Features

### Authentication

- Register.
- Login.
- Refresh token.
- Logout.
- Current user profile.

### Organization/Tenant

- Create default organization during registration.
- Associate each user with a tenant.
- Filter tenant-owned data by tenant.

### Safety Reports

Fields:

- Type: Hazard, Near Miss, Incident.
- Title.
- Description.
- Location text.
- Department text.
- Severity from 1 to 5.
- Likelihood from 1 to 5.
- Calculated risk score.
- Calculated risk level.
- Status.
- Submitted by.
- Created date.

### Risk Matrix

- Calculate score as severity x likelihood.
- Display risk level.
- Show visual matrix in frontend.

### Corrective and Preventive Actions

Fields:

- Related report.
- Title.
- Description.
- Owner.
- Due date.
- Priority.
- Status.
- Completion notes.

Statuses:

- Open.
- In Progress.
- Completed.
- Verified.

### Audit Trail

Events:

- Report created.
- Report status changed.
- Risk score calculated.
- CAPA created.
- CAPA assigned.
- CAPA status changed.
- CAPA verified.

### Dashboard

Cards:

- Open reports.
- High/Critical risk reports.
- Open CAPAs.
- Overdue CAPAs.

Charts:

- Reports by status.
- Reports by type.
- Risk level distribution.

## Non-Functional Requirements

Security:

- Password hashing.
- JWT access token.
- Refresh token rotation.
- Tenant isolation.
- Permission checks.
- Request validation.

Scalability:

- Pagination for list endpoints.
- Indexed tenant/resource columns.
- Stateless API.
- Dockerized services.
- Background-job-ready architecture.

Maintainability:

- Clean Architecture.
- Feature-based frontend.
- Testable use cases.
- Clear domain entities.
- Consistent API contracts.

Auditability:

- Important business events persisted.
- Timeline visible on report detail page.
- Created/updated metadata on core entities.

## Later Phases

Phase 2:

- File attachments.
- Email notifications.
- Background jobs for overdue CAPA reminders.
- Advanced filters.
- PDF exports.
- Safety bulletins.

Phase 3:

- Audit/inspection module.
- Configurable risk matrix.
- SignalR live updates.
- Rich investigation workflow.
- Root cause analysis templates.

Phase 4:

- RAG Safety Copilot.
- Similar incident retrieval.
- SOP and policy knowledge base.
- MCP integrations.
- Advanced observability.
