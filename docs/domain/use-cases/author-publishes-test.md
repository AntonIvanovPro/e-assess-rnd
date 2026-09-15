# Author Publishes a Test

- **Actor:** Author
- **Goal:** Assemble published Items into a Test that a Candidate can take.
- **Status:** Proposed for v0.1

## Preconditions

- At least one suitable Item is in Published status.

## Main flow

1. The Author creates a Draft Test.
2. The Author selects Items in Published status and adds them to the Test.
3. The Author requests publication.
4. The system validates the Test.
5. The system changes the Test status to Published.

## Success

A Test in Published status is available for a Test Session.

## Out of scope for v0.1

- Test sections, branching, adaptive selection, and multiple item types.
- Editing a Test in Published status. A changed Test requires a new Draft Test.
