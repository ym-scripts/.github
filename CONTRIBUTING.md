# Contributing

Thanks for helping. This guide applies to every repository in **ym-scripts** unless that repository has its own `CONTRIBUTING.md`.

## Reporting a problem

Open an issue with:

- the exact command you ran (remove any secrets or connection strings),
- what you expected and what happened, including the full output,
- your OS, shell, and the version of the tool (`--version`) and its runtime (`node -v`, `bash --version`, `php -v`).

Security issues go through [SECURITY.md](SECURITY.md), not public issues.

## Making a change

1. Fork and branch from `main`.
2. Keep the change focused. One tool, one concern.
3. Match the existing style. Each repo has an `.editorconfig`, and shell scripts must pass `shellcheck`.
4. Run the checks the repo's CI runs (see `.github/workflows/`).
5. Update the `README.md` and add an entry under **Unreleased** in `CHANGELOG.md`.
6. Open a pull request describing what changed and how you tested it.

## Design rules for tools

- Never change anything without a confirmation prompt or an explicit `--yes`. Offer `--dry-run` where it makes sense.
- Never print secrets. Read them from hidden prompts or environment variables.
- Exit codes: `0` success, `1` the operation failed, `2` usage error.
- Prefer the standard library and the platform's tools to new dependencies.
