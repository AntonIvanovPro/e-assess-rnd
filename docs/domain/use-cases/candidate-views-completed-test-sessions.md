# Candidate Views Completed Test Sessions

- **Actor:** Candidate
- **Goal:** Review the results of a previously completed Test Session.
- **Status:** Future scope

## Preconditions

- The Candidate has at least one completed Test Session.

## Main flow

1. The Candidate opens their completed Test Sessions.
2. The system shows the completed Test Sessions and their Result summaries.
3. The Candidate selects a Test Session.
4. The system shows the Result details for that Test Session.

## Success

The Candidate can review the Result of a selected completed Test Session.

## Implications for v0.1

This use case is not implemented in v0.1. However, v0.1 must preserve the facts required to implement it later:

- A Test Session is retained after it reaches a completed state.
- A Test Session has a stable Candidate identifier and Test identifier.
- A Candidate can have multiple Test Sessions for the same Test.
- A completed Test Session records its completion time and a Result reference or summary.
