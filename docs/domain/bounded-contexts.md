# Bounded Contexts

This document describes the initial domain boundaries for eAssess R&D. A bounded context owns its model, terminology, rules, and data. It is not automatically a deployable service; deployment boundaries will be decided separately.

## Context map

```text
Item Authoring → Test Assembly → Test Session Management → Test Delivery → Scoring
```

The contexts collaborate to support the v0.1 assessment lifecycle. Their shared terms are defined in the [ubiquitous language](ubiquitous-language.md).

## Item Authoring

Owns the creation and maintenance of assessment items.

- Creates and edits Items.
- Validates an Item before it is available for assessment assembly.
- Does not own Tests, Test Sessions, Candidate Answers, Scores, or Results.

## Test Assembly

Owns the composition and publication of Tests.

- Creates and edits a Test.
- Selects Items in Published status to include in a Test.
- Publishes a Test by changing its status from Draft to Published.
- Does not change the content of a Test in Published status.

## Test Session Management

Owns the lifecycle record of a Candidate taking a Test.

- Creates and manages Test Sessions for a Candidate and a Test in Published status.
- Supports immediate start in v0.1 and may support scheduling in a later version.
- Retains the Test Session after completion, including its Result reference or summary.
- Does not own Candidate Answers or calculate a Score.

Scheduling and preparation are not part of v0.1. They may become separate responsibilities only when they gain independent business rules, such as slot capacity, delivery-package creation, or asset management.

## Test Delivery

Owns the active delivery of a Test Session.

- Receives the Test structure, Item content, and delivery settings required for a Test Session.
- Presents Items and captures Candidate Answers.
- Submits answers for scoring.
- Does not own the Test Session lifecycle, decide whether answers are correct, or own the Result.

## Scoring

Owns deterministic evaluation of submitted Candidate Answers.

- Applies the scoring rules of the Test to submitted Candidate Answers.
- Produces a Score and Outcome for the Test Session.
- Does not own how a Result is stored, displayed, or published to other consumers.

## Boundary rules

- Each context owns its data and business rules.
- Contexts communicate through explicit contracts; direct access to another context's data store is prohibited.
- A Test in Published status is immutable and may be assigned to a Test Session.
- Terms must be used according to their context-specific definitions.
