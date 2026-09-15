# Domain Modeling Standards

## Purpose

eAssess R&D uses domain-driven design concepts to model the assessment domain deliberately. The approach is applied in proportion to the problem; it must clarify the system, not introduce ceremony for its own sake.

## Start with use cases

Model user goals and business behavior before choosing bounded contexts, services, storage, or integration technology. Use cases are maintained in `docs/domain/use-cases/` and release scope in `docs/releases/`.

## Ubiquitous language

The glossary in `docs/domain/ubiquitous-language.md` is the shared language for code, APIs, messages, tests, and documentation.

- Use domain terms consistently within their bounded context.
- Do not reuse a term with different meanings without explicitly qualifying it.
- UI may use a clearer user-facing label, but its mapping to the domain term must be explicit.
- QTI is a terminology baseline, not a requirement for full QTI compatibility.

## Bounded contexts

Bounded contexts own their model, business rules, language, and data. The context map in `docs/domain/bounded-contexts.md` is a living hypothesis derived from use cases.

- A bounded context is not automatically a service, database, API, or UI area.
- Contexts collaborate through explicit contracts rather than direct access to another context's data store.
- Revisit a boundary when new use cases reveal conflicting language, ownership, or lifecycle rules.

## Model only what is justified

Introduce entities, value objects, aggregates, state machines, domain events, and process managers when a use case or business invariant requires them. Do not create abstractions solely because a DDD pattern exists.

## Recording decisions

Update the ubiquitous language and relevant use cases whenever a domain term or rule changes. Record an ADR when a decision is durable, has meaningful alternatives or consequences, and affects the architecture beyond one feature.
