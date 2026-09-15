# eAssess R&D

An open-source, learning-oriented project for exploring the architecture of an e-assessment platform through deliberate AI-assisted engineering—not vibe coding—with agents operating within explicit standards, architectural boundaries, and human review. The project focuses on domain-driven design, distributed systems, and cloud.

> **Status:** early research and development. This is not a production-ready assessment platform.

## Purpose

eAssess R&D is a practical engineering lab: a deliberately small system with a complete assessment lifecycle. Its purpose is to make architectural decisions explicit, test them in running code, and document the trade-offs.

The project is designed to support discussion and learning around:

- service boundaries and storage ownership;
- synchronous and asynchronous communication;
- message contracts, versioning, retries, and idempotency;
- process managers and long-running workflows;
- immutable published Tests and eventual consistency;
- observability, integration testing, containers, and cloud deployment;
- an AI-assisted development workflow with explicit engineering standards and review roles.

## Scope: v0.1

The first release intentionally supports one small end-to-end scenario:

1. An Author creates and publishes a Single-choice Item.
2. An Author assembles and publishes a Test.
3. A Candidate starts an available Test immediately.
4. The Candidate answers the Item and submits the Test.
5. The submission is scored and a Result becomes available.

Out of scope for v0.1: scheduling, remote proctoring, complex authoring workflows, multiple item types, QTI import/export, and sophisticated psychometrics.

## Architecture direction

The target architecture will evolve in small, working increments. The initial domain areas are:

```text
Item Authoring → Test Assembly → Test Session Management
                                             ↓
                                      Test Delivery → Scoring
```

Later iterations may introduce asynchronous workflow coordination, message brokering, transactional outbox, fault handling, and distributed tracing where those concerns are justified by the scenario.

## Engineering workflow

As the repository grows, its engineering guidance will live alongside the code:

```text
agents/       AI-agent role profiles
docs/
  adr/        architecture decision records
  standards/  architecture, coding, testing, messaging, and API guidance
  domain/     domain documentation
  ui/         UI documentation
```

## Clean-room principles

This repository is an independent implementation. It must not contain or reproduce any employer or third-party proprietary code, schemas, terminology, algorithms, API contracts, documentation, or confidential business rules.

It uses publicly known assessment concepts and independently designed implementations only.
