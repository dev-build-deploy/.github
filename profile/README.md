# Develop, Build & Deploy

I'm [Kevin de Jong](https://github.com/Kevin-de-Jong). I started as a software engineer, moved into engineering
management, and returned to hands-on engineering as a Staff Engineer. Both sides taught me the same lesson: the
process work that standards like ISO and ASPICE ask for (traceable changes, versioning, release notes, licence
compliance) only works when it's automated. This organisation is where I build those tools.

## What's here

Each concern is solved once, as a library (`-it`), and offered as a tool (`-me`) you can drop into any repository:
a command-line tool, a GitHub Action, a pre-commit hook and a Claude Code plugin, all driven by the same config.

| Concern | Tool | Library |
|---|---|---|
| Commit conventions | [commit-me](https://github.com/dev-build-deploy/commit-me): Conventional Commits, in the hook and on every PR | [commit-it](https://github.com/dev-build-deploy/commit-it) |
| Versions and releases | [release-me](https://github.com/dev-build-deploy/release-me): GitHub Releases with SemVer or CalVer, changelogs, assets | [version-it](https://github.com/dev-build-deploy/version-it) |
| Licences and copyright | [reuse-me](https://github.com/dev-build-deploy/reuse-me): REUSE/SPDX compliance and an SBOM | [reuse-it](https://github.com/dev-build-deploy/reuse-it), [dep5-it](https://github.com/dev-build-deploy/dep5-it) |
| Secrets | [secret-me](https://github.com/dev-build-deploy/secret-me): no token, key or password reaches a repository | |
| Planning | [plan-me](https://github.com/dev-build-deploy/plan-me): a backlog on GitHub issues and Projects | |
| Documentation | [docs-me](https://github.com/dev-build-deploy/docs-me): repository docs published to the wiki | |
| Diagnostics | | [diagnose-it](https://github.com/dev-build-deploy/diagnose-it), [sarif-it](https://github.com/dev-build-deploy/sarif-it), [comment-it](https://github.com/dev-build-deploy/comment-it) |

The Claude Code plugins are collected in one marketplace: [claude-plugins](https://github.com/dev-build-deploy/claude-plugins).

## How they're built

- **Deterministic.** No tool depends on AI to do its job. They're built so people and coding agents can both use
  them well: compact or JSON output, safe to run twice.
- **Standards, not inventions.** Conventional Commits, Semantic Versioning, REUSE and SPDX, SARIF, Keep a Changelog.
- **Caught before CI.** Every check exists as a pre-commit hook and an agent plugin as well as a CI step, so a
  mistake is fixed where it's made.
- **Used on themselves.** Every repository here runs these tools on itself: its commits, licences, secrets and
  releases.

## Why

In regulated software these processes are mandatory and often dreaded. I want them to be cheap, automatic and
invisible until something's actually wrong.
