# Contributing

General rules for the organization's repositories. This is an **org-level
default** — each repository has its own `CONTRIBUTING.md` with the details, which
takes precedence on any conflict.

## A single toolchain

The platform's code repositories follow one standard:

- **`uv`** — the only package manager (`pyproject.toml` + `uv.lock`); no
  `requirements.txt`, no manual `.venv` activation.
- **`make`** — orchestration: every task is run via `make <target>`, not by
  calling tools directly (versions and flags stay in sync across local,
  pre-commit, and CI).
- **`make check`** — the single quality gate. The same set of checks runs
  locally, in pre-commit, and in CI; it is adapted to each repository's content.
- **pre-commit** — three layers of defense: local → pre-commit → CI.
- **Conventional Commits** — mandatory; header format is an English prefix plus a
  Russian subject (e.g. `feat(scope): добавить порог`). Versions and
  `CHANGELOG.md` are managed by `python-semantic-release` — never edit them by
  hand.

## Workflow

1. Branch off the default branch (do not commit to it directly).
2. Make sure `make check` is green locally.
3. Open a PR; the title follows Conventional Commits.
4. Wait for green CI and review.

For repository-specific details, see that repository's own `CONTRIBUTING.md`,
`README.md`, and `CLAUDE.md`.
