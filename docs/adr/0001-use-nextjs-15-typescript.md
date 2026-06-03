# ADR 0001: Use Next.js 15 with TypeScript

- **Status:** Accepted
- **Date:** 2026-06-03

## Context

The photo gallery application needs a modern React framework that supports server rendering, file-based routing, production builds, and a smooth developer experience. The codebase also benefits from strong typing because UI components, mock data, and future API contracts are shared across multiple pages.

## Decision

Use **Next.js 15** with the **App Router** and **TypeScript** as the primary application stack.

## Rationale

- Next.js 15 provides an opinionated production framework for routing, layouts, metadata, and deployment.
- TypeScript improves safety for component props, page composition, and future API modeling.
- The current repository already depends on React 19, Next.js 15.4.4, and TypeScript 5, making this the natural platform choice.
- The App Router fits the current page structure under `src/app` and keeps routing conventions simple.

## Consequences

### Positive

- Strong typing for reusable UI components and mock data structures.
- Built-in support for optimized builds, layouts, and deployment to common hosting platforms.
- Clear project structure for onboarding and documentation.

### Trade-offs

- Next.js upgrades can affect linting, build behavior, and deployment expectations.
- Some runtime behavior, such as remote font fetching, may differ between local, CI, and sandboxed environments.

## Alternatives considered

- **Plain React with Vite:** lightweight, but would require more manual setup for routing, metadata, and deployment conventions.
- **JavaScript without TypeScript:** lower initial friction, but weaker guarantees for shared props and data models.
