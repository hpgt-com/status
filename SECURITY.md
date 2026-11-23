# Security

## Reporting a security issue

Do not open a public issue. Use **Report a vulnerability** under this repository's **Security** tab, so only the
maintainers see the report. Describe what you found, how to reproduce it and what it affects. We reply as soon as we
can, but this is a volunteer club project.

## What is in place

- All changes to `main` go through a pull request (branch ruleset «Main protection»). Force push and deletion of `main`
  are blocked.
- Required checks: `dependency-review` (no dependencies with known vulnerabilities) and `workflow-security` (zizmor),
  plus CodeQL code scanning (high or higher blocks the merge).
- Actions are pinned to commit SHAs and updated monthly by Dependabot, with a 7-day cooldown.
- Workflows get read-only access by default; jobs ask for more only when they need it.
- Secrets live in GitHub environments limited to `main`, never in the code. `.gitignore` blocks `.env` and key files.
- Secret scanning with push protection, Dependabot alerts and security updates are on.

## Specific to this repository

- Upptime commits its results to `main` with a token from the GitHub App «HPGT Status». The token lasts one hour,
  covers only this repository and has only Contents and Issues. The app key is in the environment `status` (only
  `main`).
- The jobs that commit keep that token in the checkout. The other jobs use `persist-credentials: false`.
- The app is the only bypass in the ruleset for `main`.
- The status page is served by GitHub Pages, which cannot set security headers. The page is static, with no forms,
  cookies or third-party scripts.
