# 001 — Use Domain-Driven Design for Domain Modeling

- **Status:** Accepted
- **Date:** 2026-09-15

## Context

An e-assessment platform has distinct business lifecycles and responsibilities, including item authoring, test assembly, test sessions, delivery, and scoring. Starting from technical layers or deployable services would risk coupling unrelated rules and terminology.

## Decision

Use domain-driven design concepts as the primary approach for understanding and structuring the domain.

The project will begin with use cases and ubiquitous language, then derive and revise bounded contexts. Contexts own their rules, models, terminology, and data. Their interactions will use explicit contracts.

## Consequences

- Domain documents are maintained alongside code in `docs/domain/`.
- Current bounded contexts are hypotheses and may change as use cases evolve.
- A bounded context does not imply a separate microservice, database, UI, or deployment unit.
- Services, integration patterns, and storage are chosen later according to concrete use cases and non-functional requirements.
- DDD patterns are used only when they make a domain rule or boundary clearer.
