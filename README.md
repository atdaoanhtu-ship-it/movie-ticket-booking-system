# CineBook — Movie Ticket Booking System

CineBook is a full-stack movie ticket booking platform built with Next.js and NestJS.

The project focuses on designing and implementing a reliable ticket booking system, particularly handling concurrent seat reservations, booking lifecycles, and payment processing.

**Project Status:** In Development — Initial Setup

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Backend | NestJS, TypeScript |
| Database (Planned) | PostgreSQL |
| ORM (Planned) | Prisma |
| Monorepo | npm workspaces |
| Version Control | Git & GitHub |

## Project Structure

```text
movie-ticket-booking-system/
├── apps/
│   ├── api/             # NestJS backend
│   └── web/             # Next.js frontend
├── docs/                # Project documentation (planned)
├── AGENTS.md            # AI development guidelines
├── package.json         # Root workspace configuration
└── package-lock.json
```

## Getting Started

### Prerequisites

- Node.js 22.23.3
- npm

### Installation

Clone the repository and install dependencies from the project root:

```bash
npm install
```

### Run Backend

```bash
npm run dev:api
```

Default backend URL: `http://localhost:3000`

### Run Frontend

Open another terminal:

```bash
npm run dev:web
```

Next.js commonly uses `http://localhost:3000`, but the actual port may differ if the backend is already using that port. The final development ports will be configured later.

## Development Roadmap

- [ ] Analyze business requirements and actors
- [ ] Design screen flows and use cases
- [ ] Design database schema and relationships
- [ ] Implement movie, cinema, and showtime management
- [ ] Implement seat availability and reservation
- [ ] Handle concurrent seat reservations
- [ ] Implement booking and payment simulation
- [ ] Add automated tests and CI/CD
- [ ] Prepare future multi-tenant marketplace support

## Architecture

CineBook follows a Modular Monolith architecture.

The initial implementation focuses on core ticket booking. The domain model will include minimal partner ownership relationships to support future multi-tenancy, while partner authorization and marketplace management are deferred.

## Development Workflow

Requirement → Design → Implementation → Testing → Deployment

Development is organized using GitHub Issues, feature branches, Pull Requests, and Conventional Commits.