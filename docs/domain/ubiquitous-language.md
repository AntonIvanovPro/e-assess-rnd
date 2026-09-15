# Ubiquitous Language

This glossary is the shared vocabulary for the v0.1 domain. Terms must be used consistently in code, APIs, messages, tests, and documentation. A term with a context-specific meaning must be qualified or replaced rather than reused ambiguously.

## QTI terminology

Domain terminology is based on the IMS Question and Test Interoperability (QTI) standard, with deliberate restrictions for this project.

eAssess R&D adopts only the concepts required by its current scope. Its simplified Item and Test terms are based on QTI assessment item and assessment test concepts. QTI terminology does not imply full QTI compatibility, support for every QTI feature, or QTI import/export.

## Item Authoring

| Term | Definition |
| --- | --- |
| Item | An independently authored and publishable unit of assessment content. It may contain content, interactions, scoring rules, assets, metadata, and other information required by the supported item type. |
| Single-choice Item | An Item for which a candidate selects one answer option. This is the only supported item type in v0.1. |
| Answer Option | A selectable response within a Single-choice Item. |
| Correct Answer | The Answer Option designated as correct for an Item. |

## Test Assembly

| Term | Definition |
| --- | --- |
| Test | A composition of Items and rules that govern their delivery, including settings relevant to taking the Test. A Test is mutable while it is in Draft status. |
| Published | A status of an Item or Test that indicates it is available for its next domain use. A Test in Published status is immutable. |
| Publish | The action that changes an Item or Test status from Draft to Published. |

## Test Session Management

| Term | Definition |
| --- | --- |
| Candidate | A person who may take a Test in Published status. |
| Test Session | A candidate-specific instance of taking a Test. It is created when a Candidate starts a Test immediately or schedules it, and persists until it reaches a terminal state. |

## Test Delivery

| Term | Definition |
| --- | --- |
| Candidate Answer | The response selected by a Candidate for an Item during a Test Session. |
| Submit | The action that completes active delivery and sends Candidate Answers for scoring. |

## Scoring

| Term | Definition |
| --- | --- |
| Score | The calculated value produced by evaluating submitted Candidate Answers. |
| Outcome | The interpretation of a Score according to Test rules, such as Passed or Failed. |
| Scoring | The process of evaluating submitted Candidate Answers to produce a Score and Outcome. |
| Result | The Score and Outcome recorded for a completed Test Session and made available to the Candidate. |
