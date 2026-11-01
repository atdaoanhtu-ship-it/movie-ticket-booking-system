# CineBook — AI Development Guidelines

## 1. Project Overview

CineBook is a movie ticket booking platform.

The initial goal is to build a reliable core booking system, focusing on seat reservations, concurrency control, booking lifecycle, and payment processing.

The architecture should allow future marketplace and multi-tenant capabilities without implementing them in the initial phase.

## 2. Tech Stack

- Frontend: Next.js + TypeScript
- Backend: NestJS + TypeScript
- Database: PostgreSQL
- ORM: Prisma
- Package Manager: npm workspaces
- Architecture: Modular Monolith
- Version Control: Git + GitHub

## 3. Repository Structure

- `apps/web` — Frontend application
- `apps/api` — Backend application
- `docs` — Requirements, architecture, and design documentation

## 4. Architecture Rules

- Keep business logic in the backend.
- Keep NestJS controllers thin.
- Organize backend code by business modules.
- Do not introduce microservices without an approved architectural decision.
- Prepare for future multi-tenancy with a minimal Partner ownership model.
- Do not implement tenant authorization, partner dashboards, or marketplace management until requested.
- Use PostgreSQL transactions and database constraints to protect critical booking operations.
- Never rely solely on frontend state to determine seat availability.

## 5. Development Workflow

Follow this process:

Requirement → Design → Implementation → Testing → Deployment

Before implementing a feature:

1. Read the relevant documentation.
2. Understand the current GitHub Issue and acceptance criteria.
3. Propose the implementation approach.
4. Identify affected files and modules.
5. Confirm significant architectural changes before coding.

## 6. Coding Rules

- Use TypeScript.
- Prefer clear, maintainable code over unnecessary abstractions.
- Do not modify unrelated files.
- Do not introduce dependencies without justification.
- Do not change database schemas without migrations.
- Write tests for important business rules.
- Never commit credentials, secrets, or local environment files.
- Follow the root Prettier configuration.

## 7. Git Workflow

- Use `main` as the primary branch.
- Create short-lived branches for individual tasks or features.
- Follow Conventional Commits.
- Open Pull Requests before merging into `main`.
- Keep Pull Requests focused and reviewable.

## 8. AI Collaboration Rules

- Act as a technical mentor and development assistant.
- Explain important technical decisions and trade-offs.
- Do not generate an entire feature without understanding its requirements.
- Ask for clarification when business rules are ambiguous.
- Do not silently change architecture or project scope.
- Prioritize helping the developer understand the implementation rather than merely producing code.