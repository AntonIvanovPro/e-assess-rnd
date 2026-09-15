# Information Architecture

This is the initial navigation hypothesis derived from v0.1 use cases. It describes user-facing areas and transitions, not service or deployment boundaries.

## Author Workspace

```text
Items
  ├─ Items list
  ├─ Item editor
  └─ Item details

Tests
  ├─ Tests list
  ├─ Test editor
  ├─ Item picker
  └─ Test details
```

An Author creates and edits Items and Tests in their Draft status. Item and Test details show their current status, including Published.

## Candidate Portal

```text
Available Tests
  └─ Test details
       └─ Test delivery
            └─ Result
```

The Candidate selects an available Test, starts it immediately, completes delivery, and views the Result.

## Future Navigation

```text
My Test Sessions
  └─ Test Session details
       └─ Result details

Test details
  └─ Schedule a Test
```

Test Session history and scheduling are deliberately outside the v0.1 navigation scope.
