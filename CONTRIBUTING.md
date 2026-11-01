# Contributing to dev-build-deploy

Thank you for helping. These rules apply to every repository in the organisation unless it has its own
`CONTRIBUTING.md`. Each rule is checked by one of our own tools, in a pre-commit hook and in CI, so you hear
about a mistake before a reviewer does.

## Before you start

For anything bigger than a small fix, open an issue first so we can agree on the idea.

After cloning a tool repository, install the git hooks once:

```sh
npm run setup-hooks   # runs: pre-commit install --hook-type pre-commit --hook-type commit-msg
```

You need [pre-commit](https://pre-commit.com) installed (`brew install pre-commit`).

## The rules

| Rule | Checked by |
|---|---|
| **Conventional Commits** for every commit message: `type(scope): summary` | [commit-me](https://github.com/dev-build-deploy/commit-me) |
| **REUSE**: every file has an SPDX copyright and licence header | [reuse-me](https://github.com/dev-build-deploy/reuse-me) |
| **No secrets**: no token, key or password in a commit | [secret-me](https://github.com/dev-build-deploy/secret-me) |
| **Pull request description** with four sections: Why, How, Review hints, Proof | [pull-me](https://github.com/dev-build-deploy/pull-me) |
| **Signed commits** (SSH or GPG): GitHub shows them as Verified | repository rules |
| **Squash merge**: the pull request title becomes the commit, so it follows Conventional Commits too | repository settings |

The four sections of a pull request (the [template](https://github.com/dev-build-deploy/.github/blob/main/.github/PULL_REQUEST_TEMPLATE.md) is filled in for you):

- **Why**: the value, for whom, and which issue asks for it.
- **How**: what you built and why you chose it.
- **Review hints**: where the risk is and what to read first.
- **Proof**: real evidence, such as test output or links to CI runs.

Write for a junior engineer who is new to the repository: plain words, short sentences.

## Pull requests

1. Branch from `main`, make small commits, push, open a pull request.
2. Wait for the checks to pass (`gh pr checks`).
3. A maintainer reviews and squash-merges. Please do not merge your own pull request.

## Security

Do not report vulnerabilities in public issues. See [SECURITY.md](https://github.com/dev-build-deploy/.github/blob/main/SECURITY.md).
