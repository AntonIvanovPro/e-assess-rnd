# Version Control Standards

## Adopted Public Approaches

### GitHub Flow

Follow [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow): create a branch for each unrelated change, open a pull request, merge it into `main`, then delete the branch.

### Conventional Commits

Follow [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) for commit messages:

```text
<type>[optional scope]: <description>
```

Use `feat` for a feature and `fix` for a bug fix, as defined by the specification.

## eAssess R&D Additions

### Branch names

Use lowercase kebab-case names in this format:

```text
<type>/<short-description>
```

Allowed types: `feature`, `fix`, `docs`, `refactor`, `chore`, and `experiment`.

Example: `feature/author-publishes-item`.

### Commit messages

Use these additional types when applicable: `docs`, `test`, `refactor`, `build`, `ci`, and `chore`.

Keep the description lowercase, specific, under 72 characters, and without a final period.

Each commit represents one coherent change. Add a body when the reason or trade-off is not clear from the summary.
