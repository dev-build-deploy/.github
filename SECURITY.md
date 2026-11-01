# Security policy

## Reporting a vulnerability

Please do not open a public issue for a security problem.

Report it privately with GitHub's private vulnerability reporting, per repository:

1. Open the repository the problem is in (for example `dev-build-deploy/commit-me`).
2. Go to the **Security** tab and choose **Report a vulnerability**.
3. Describe what you found, how to reproduce it and what it could allow.

If the repository does not show that button, open an issue that only says you need a private channel (no
details) and a maintainer will enable it or contact you.

We aim to reply within a week, fix confirmed problems in a new release, and credit you if you want.

## Supported versions

Only the **latest release of each tool** receives security fixes. Upgrade to it before reporting, if you can.
The Claude Code plugins in [claude-plugins](https://github.com/dev-build-deploy/claude-plugins) follow the
release of the tool they wrap.

## Found a leaked secret?

If you see a token, key or password in any dev-build-deploy repository, report it the same way, and rotate it
if it is yours.
