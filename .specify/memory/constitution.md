<!--
Sync Impact Report:
- Version change: 0.0.0 -> 1.0.0
- Modified principles: template placeholders -> Student-Centered Product Integrity, Type-Safe Engineering Standards, Next.js Architecture Discipline, Tailwind-First Interface Consistency, Test-First Quality and Reliability, Clear Naming and Team Collaboration
- Added sections: Additional Constraints, Development Workflow
- Removed sections: none
- Templates requiring updates:
  - .specify/templates/plan-template.md ✅ reviewed; no direct change required
  - .specify/templates/spec-template.md ✅ reviewed; no direct change required
  - .specify/templates/tasks-template.md ✅ reviewed; no direct change required
  - .specify/templates/commands/ ⚠ not present in this workspace snapshot
- Follow-up TODOs: none
-->

# Student Planner Constitution

## Core Principles

### I. Student-Centered Product Integrity
Student Planner exists to help students manage schedules, assignments, deadlines, and study routines with clarity and confidence. Every feature MUST support real student workflows, reduce planning friction, and preserve trust through accessible, predictable experiences. If a requirement adds complexity without improving user value, it MUST be simplified or rejected.

### II. Type-Safe Engineering Standards
All application logic MUST use TypeScript in strict mode. Variables, function parameters, and return values MUST be explicitly typed unless inference is clear and safe. The `any` type is forbidden; when data shapes are uncertain, define precise interfaces, unions, or utility types. Code that cannot be type-checked cleanly MUST be fixed before merge.

### III. Next.js Architecture Discipline
The application MUST use Next.js App Router conventions. Server components are the default for data fetching, business logic, and page composition; client components are used only when required for browser APIs, event handlers, or client state. File-based routing MUST drive navigation structure, and shared layout, page, loading, and error boundaries MUST be used consistently. Route and component boundaries MUST reflect student workflows and remain easy to reason about.

### IV. Tailwind-First Interface Consistency
UI work MUST follow a utility-first Tailwind CSS approach. Reusable styling should come from Tailwind classes and design tokens, not bespoke CSS files, unless a requirement genuinely requires a targeted stylesheet or a third-party library. Components MUST remain responsive, accessible, and consistent with the product design system. Custom CSS is an exception, not the default.

### V. Test-First Quality and Reliability
Every meaningful feature, bug fix, validation rule, and user workflow MUST be backed by automated tests before deployment. The team MUST prefer unit tests for isolated logic, component tests for rendering and interaction, and integration tests for data flow and route behavior. Tests MUST fail before the fix and pass after, and release-worthy work MUST include evidence of validation.

### VI. Clear Naming and Team Collaboration
Code, files, branches, and API contracts MUST use descriptive, consistent names that match the domain language of a planner: task, course, deadline, calendar, study session, and schedule. Avoid vague abbreviations or framework-specific names where domain terms are clearer. Pull requests MUST be reviewed for correctness, accessibility, performance, and maintainability; engineering decisions MUST be documented when they affect architecture, data modeling, or product behavior.

## Additional Constraints

- The application MUST be built with Next.js App Router, TypeScript, and Tailwind CSS.
- TypeScript MUST run with strict mode enabled and the repository MUST reject `any` in application code.
- Components MUST be organized around student workflow boundaries rather than implementation convenience.
- Custom CSS MUST be minimized and justified in writing when introduced.
- Accessibility and responsive behavior are non-negotiable for schedule, task, and academic planning flows.
- Data and UI state MUST be treated as explicit contracts and validated before rendering or persistence.
- The project MUST favor small, composable, easily testable units over large, tightly coupled components.

## Development Workflow

- Feature work begins with a clear user need, acceptance criteria, and testing strategy.
- Design, implementation, and validation MUST align with the constitution’s principles before merge.
- Pull requests MUST include evidence of relevant tests, a summary of behavior changes, and any migration or configuration notes.
- Breaking changes to data, routes, or user flows MUST be documented and communicated before release.
- Reviewers MUST verify architecture alignment, naming clarity, and TypeScript/Tailwind compliance before approval.
- The team MUST keep documentation and examples current so onboarding and future iterations remain predictable.

## Governance
This constitution governs all Student Planner implementation decisions. It supersedes local preferences or ad hoc patterns when they conflict with these rules. Any exception MUST be explicit, time-bound, and justified with a business, technical, or accessibility rationale.

Amendments require a written proposal, team review, and a recorded version change. The project MUST use semantic versioning for constitutional changes:
- MAJOR: backward-incompatible rule changes or removal of core principles
- MINOR: new principle or materially expanded guidance
- PATCH: wording clarifications, typo corrections, and non-semantic refinements

Compliance is reviewed by examining code, tests, architecture decisions, and pull request quality. If work violates the constitution, the team MUST correct the issue before merge or document a justified exception with explicit approval.

**Version**: 1.0.0 | **Ratified**: 2026-09-26 | **Last Amended**: 2026-09-26
