# ym-scripts/.github

Organisation-wide files for [ym-scripts](https://github.com/ym-scripts).

| Path | Purpose |
| --- | --- |
| `profile/README.md` | The organisation's public profile page |
| `profile/logo.svg`, `profile/logo.png` | Logo (use the PNG as the organisation avatar) |
| `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `SUPPORT.md` | Default community files for every repo that doesn't have its own |
| `ISSUE_TEMPLATE/`, `PULL_REQUEST_TEMPLATE.md` | Default issue and PR templates |

## Adding a new tool

1. Create a repo named after the command, for example `ym-scripts/db-backup`.
2. Put the entry script at the root. Add a `package.json` with a `bin` entry so `npx github:ym-scripts/<tool>` works. A bash script with a `#!/usr/bin/env bash` shebang can be the `bin` target directly.
3. Include `README.md` (install/run, options, exit codes), `LICENSE`, `CHANGELOG.md` and a CI workflow (lint plus a smoke test).
4. Tag releases as `vX.Y.Z` and add the tool to the table in `profile/README.md`.
