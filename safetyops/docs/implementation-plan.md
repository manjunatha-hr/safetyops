# Two-Weekend Implementation Plan

## Strategy

Build a narrow but polished vertical slice. The MVP should prove enterprise engineering quality rather than trying to implement every SMS feature.

## Weekend 1: Backend Foundation

### Day 1

- Create .NET solution.
- Add Clean Architecture projects.
- Configure PostgreSQL with EF Core.
- Add Docker Compose for database.
- Implement base entities and audit metadata.
- Add authentication endpoints.
- Implement JWT and refresh tokens.
- Add tenant model.

### Day 2

- Implement safety report module.
- Implement risk scoring.
- Implement CAPA module.
- Add audit event creation.
- Add dashboard summary query.
- Add Swagger.
- Add basic unit tests for risk scoring and workflow transitions.

## Weekend 2: Frontend and Polish

### Day 3

- Create React + TypeScript app.
- Add routing and auth screens.
- Add API client and token handling.
- Build dashboard page.
- Build report list and create report page.
- Build report detail page with risk and audit timeline.

### Day 4

- Build CAPA list and update screens.
- Add role/permission-aware UI.
- Improve styling and responsive layout.
- Add seed/demo data.
- Add README screenshots and architecture notes.
- Run full local verification through Docker Compose.

## Stretch Goals

Only add these if the MVP is stable:

- File attachments.
- Email notification mock.
- Background job for overdue CAPAs.
- SignalR status updates.
- PDF report export.

## Definition of Done

- App runs locally with one command or clear setup steps.
- User can register and log in.
- Tenant isolation exists in backend queries.
- User can create and view a safety report.
- Risk level is calculated and displayed.
- User can create and update CAPAs.
- Dashboard shows real data.
- Audit timeline records key events.
- README explains project value and architecture.

