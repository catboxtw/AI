# Vendored skills

Some skills under `.claude/skills/` are copied from upstream projects so that
cloud sessions (claude.ai/code) can load them — cloud sessions clone the repo
but do not install plugins enabled in `.claude/settings.json`.

## frontend-design
- Source: https://github.com/anthropics/claude-plugins-official (plugins/frontend-design)
- License: see `frontend-design/LICENSE.txt`

## Strix security skills (9)
- Source: https://github.com/usestrix/strix (skills/)
- License: Apache-2.0, see `LICENSE.strix.txt`
- Skills: api-security-testing, application-security-testing,
  ci-security-scanning-with-strix, find-security-vulnerabilities-in-code,
  fix-security-vulnerabilities-with-strix, managed-pentesting-with-strix,
  owasp-top-10-testing, penetration-testing-with-strix,
  web-app-penetration-testing
- Runtime: these skills drive the Strix engine, which needs a running Docker
  daemon and an LLM API key. They load in any session, but a scan only runs
  where Docker is available (e.g. local Windows with Docker Desktop), not in a
  cloud session without a Docker daemon.
