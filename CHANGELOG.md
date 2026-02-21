# Changelog

All notable changes to this template will be documented in this file.

This project adheres to [Semantic Versioning](https://semver.org) and the format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [Unreleased]

### Added

- Initial template structure with full `docs/` directory
- Documentation files: `01-overview`, `02-objectives`, `03-requirements`, `04-architecture`, `05-data-model`, `06-api-contracts`, `07-security`, `08-quality`, `09-observability`, `10-glossary`, `11-references`
- `docs/12-deployment.md` — Deployment documentation: environments, CI/CD pipeline, release strategy (blue-green/canary/rolling), rollback plan, infrastructure, post-deploy monitoring
- `docs/13-decisions-log.md` — Lightweight decisions log as an alternative to formal ADRs
- ADR structure with usage guide (`docs/adr/README.md`) and blank template (`docs/adr/001-template.md`)
- Diagram templates using Mermaid: C4 Context (L1), C4 Container (L2), C4 Component (L3), Deployment, ER Diagram, Sequence Flows, State Diagram
- Design documentation placeholder (`docs/design/README.md`)
- `CONTRIBUTING.md` — Contribution guide: GitHub Flow branching strategy, Conventional Commits convention, pull request process, and code review guidelines
- `CODE_OF_CONDUCT.md` — Contributor Covenant Code of Conduct (v2.1)
- `SECURITY.md` — Responsible disclosure policy; detected automatically by GitHub to display the "Report a vulnerability" button
- `mkdocs.yml` — Optional MkDocs + Material theme config to serve the docs as a website
- `.env.example` — Documented environment variables with placeholder values for local setup
- `.markdownlint.json` — Markdownlint configuration tuned for this template's writing style
- `.github/workflows/ci.yml` — CI workflow: markdown linting and link checking on every push and pull request
- `.github/link-check-config.json` — Link checker configuration (ignores shields.io badges and TODO placeholders)
- `docs/index.md` — MkDocs landing page summarising all documentation sections
- GitHub issue templates: bug report, feature request, task
- `PULL_REQUEST_TEMPLATE.md`
- MIT License
- This CHANGELOG

### Changed

- `docs/04-architecture.md` — Deployment Model section links to both the deployment diagram and `12-deployment.md`
- `docs/diagrams/README.md` — Diagram index includes all 7 diagram types
- `docs/adr/README.md` — ADR index no longer lists the blank template as an "Accepted" decision
- `mkdocs.yml` — Fixed `Home` navigation entry from invalid `../README.md` to `index.md`

---

## How to Update This File

When making changes to the template, add an entry under `[Unreleased]` using one of the following categories:

- **Added** — new files or sections introduced to the template
- **Changed** — changes to existing content or structure
- **Deprecated** — sections or files that will be removed in a future version
- **Removed** — files or sections that were removed
- **Fixed** — corrections to placeholders, links, or instructions

When releasing a new version, move the contents of `[Unreleased]` to a new versioned section, tag the commit in Git, and reset `[Unreleased]` to empty.

```bash
git tag -a v1.0.0 -m "release: v1.0.0"
git push origin v1.0.0
```

