# SafeSphere SMS

SafeSphere SMS is a portfolio-grade Safety Management System platform for small and mid-sized organizations. It is inspired by corporate SMS practices used in safety-critical industries, with a focused MVP around reporting, risk scoring, corrective actions, audit trails, and dashboard analytics.

The first version is intentionally scoped as a polished vertical slice that can be completed quickly while still demonstrating enterprise-grade full-stack engineering.

## Product Vision

SafeSphere helps organizations move from reactive incident handling to proactive safety risk management.

Core capabilities:

- Report hazards, near misses, and incidents.
- Assess risk using a severity x likelihood matrix.
- Assign and track corrective and preventive actions.
- Maintain an audit timeline for important workflow events.
- Provide tenant-isolated dashboards for safety managers and executives.
- Prepare for future AI-assisted safety knowledge retrieval using RAG and MCP integrations.

## MVP Scope

The first implementation will focus on:

- Authentication with JWT and refresh tokens.
- Multi-tenant organization model.
- Role and permission-based authorization.
- Incident, hazard, and near-miss reporting.
- Risk score calculation and risk level classification.
- CAPA workflow for corrective/preventive actions.
- Audit trail events for key business actions.
- Safety dashboard with operational metrics.
- Dockerized local development.

Out of scope for the first version:

- Full regulatory compliance certification.
- Complex configurable workflows.
- Production email/SMS delivery.
- Full document management.
- AI/RAG assistant.
- MCP integrations.
- Advanced observability stack.

These are kept as planned extensions so the architecture can evolve without bloating the MVP.

## Target Users

- Reporter: submits hazards, near misses, and incidents.
- Supervisor: triages reports and monitors department actions.
- Safety Manager: owns risk assessment, CAPA tracking, and closure decisions.
- Investigator: documents incident investigation details.
- Action Owner: completes assigned corrective/preventive actions.
- Auditor: reviews audit history and evidence.
- Executive Viewer: reads dashboards and high-risk summaries.
- System Admin: manages tenant configuration, users, and permissions.

## Tech Stack

Frontend:

- React
- TypeScript
- Vite
- React Router
- TanStack Query
- React Hook Form
- Zod
- Charting library such as Recharts or ECharts

Backend:

- .NET Web API
- Clean Architecture
- Entity Framework Core
- PostgreSQL
- MediatR/CQRS
- FluentValidation
- JWT authentication
- Permission-based authorization
- Serilog
- Swagger/OpenAPI

Infrastructure:

- Docker Compose
- PostgreSQL
- Redis, optional in MVP
- Background jobs with Hangfire or Quartz, optional in MVP

Future AI/Integration:

- RAG over safety manuals, SOPs, incident history, and audit reports.
- Vector storage with pgvector or Qdrant.
- MCP integrations for documents, ticketing, calendar, and enterprise systems.

## Repository Structure

```text
safe-sphere-sms/
  backend/
    src/
    tests/
  frontend/
    src/
  docs/
    architecture.md
    product-scope.md
    implementation-plan.md
  docker-compose.yml
  README.md
```

## Success Criteria

The MVP is considered complete when a user can:

1. Register or log in.
2. Work inside an isolated organization/tenant.
3. Submit a safety report.
4. View calculated risk level.
5. Create and assign CAPA items.
6. Update workflow status.
7. See audit trail events.
8. Use a dashboard to understand open risk and overdue work.

## Resume Positioning

Suggested resume description:

Built a multi-tenant Safety Management System using React, TypeScript, .NET Web API, PostgreSQL, JWT authentication, permission-based authorization, EF Core, CQRS, Docker, and audit logging. Implemented safety reporting, risk scoring, CAPA workflow, dashboard analytics, and tenant-isolated data access.

