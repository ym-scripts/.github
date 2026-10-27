<p align="center">
  <img src="https://raw.githubusercontent.com/ym-scripts/.github/main/profile/logo.svg" width="96" alt="ym-scripts logo">
</p>

<h3 align="center">ym-scripts</h3>

<p align="center">
  Small, focused developer scripts you can run straight from GitHub, with nothing to install and no package registry involved.
</p>

---

Each repository is one tool. Run any of them without cloning:

```bash
npx github:ym-scripts/<tool>            # Node, or anything with a bin wrapper
npx github:ym-scripts/<tool>#v1.2.0     # pin a released version (git tag)
curl -fsSL https://raw.githubusercontent.com/ym-scripts/<tool>/main/<script>.sh | bash
```

### Tools

| Tool                                                                     | What it does                                                                               | Run it                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | --------------------------------------------------- |
| [**pg-migrate**](https://github.com/ym-scripts/pg-migrate)               | Copy one Postgres database into another, with pre-flight checks and row-count verification | `npx github:ym-scripts/pg-migrate`                  |
| [**portless-x-herd**](https://github.com/ym-scripts/portless-x-herd)     | Clean `https://<app>.web.test` URLs for Node dev servers alongside Laravel Herd            | `npx github:ym-scripts/portless-x-herd`             |
| [**enable-dependabot**](https://github.com/ym-scripts/enable-dependabot) | Turn on Dependabot alerts and security updates for every repo you own                      | `npx github:ym-scripts/enable-dependabot --dry-run` |
| [**pg-backup**](https://github.com/ym-scripts/pg-backup) | Scheduled PostgreSQL backups to disk and S3/R2, with retention, checksums and one-command restore | `npx github:ym-scripts/pg-backup --help` |
| [**mysql-backup**](https://github.com/ym-scripts/mysql-backup) | The same for MySQL and MariaDB | `npx github:ym-scripts/mysql-backup --help` |
| [**env-check**](https://github.com/ym-scripts/env-check) | Compare `.env` with `.env.example`: missing, empty and extra keys, without printing values | `npx github:ym-scripts/env-check` |
| [**doppler-to-eas**](https://github.com/ym-scripts/doppler-to-eas) | Copy Doppler secrets into Expo EAS environments with the right visibility | `npx github:ym-scripts/doppler-to-eas dev --dry-run` |

### Principles

- **Safe by default.** Destructive steps ask for confirmation and support `--dry-run`.
- **Few dependencies.** Each tool uses the platform's standard tools and nothing else where possible.
- **Readable.** Each tool is one script you can read before you run it.
- **Versioned.** Every tool is tagged with [SemVer](https://semver.org), so you can pin with `#vX.Y.Z`.

<sub>Maintained by <a href="https://github.com/YoungMayor">@YoungMayor</a> · MIT licensed</sub>
