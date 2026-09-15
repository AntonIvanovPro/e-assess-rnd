# User Flows

This document represents use cases from a user's perspective. It validates user journeys, terminology, commands, and information needs; it does not prescribe UI technology, service boundaries, or deployment architecture.

The navigation areas and transitions are defined in [information architecture](information-architecture.md).

## Author publishes a Single-choice Item

**Use case:** [Author publishes a Single-choice Item](../domain/use-cases/author-publishes-single-choice-item.md)

```text
Items list → Item editor → Validation feedback → Item details (Published)
```

The Item editor supports the v0.1 Single-choice Item: content, answer options, and Correct Answer.

## Author publishes a Test

**Use case:** [Author publishes a Test](../domain/use-cases/author-publishes-test.md)

```text
Tests list → Test editor → Item picker → Validation feedback → Test details (Published)
```

The Item picker shows only Items in Published status. A Test in Published status is read-only.

## Candidate takes a Test immediately

**Use case:** [Candidate completes a Test immediately](../domain/use-cases/candidate-completes-test-immediately.md)

```text
Available Tests → Test details → Start now → Test delivery → Submit → Result
```

The initial Available Tests view may be a simple list. Search, filtering, eligibility explanations, and scheduling are not part of v0.1.

## Candidate views completed Test Sessions

**Use case:** [Candidate views completed Test Sessions](../domain/use-cases/candidate-views-completed-test-sessions.md)

```text
My Test Sessions → Completed Test Sessions → Test Session details → Result details
```

This is future scope. It confirms that a completed Test Session and its Result must remain queryable after delivery ends.

## Candidate schedules a Test

**Use case:** [Candidate schedules a Test](../domain/use-cases/candidate-schedules-test.md)

This future flow is intentionally unspecified until slot capacity, scheduling, cancellation, and rescheduling rules are decided.
