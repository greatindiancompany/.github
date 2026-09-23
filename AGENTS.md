# AGENTS.md

Instructions for Cursor Cloud Agents working in this repository.

## What this repo is

`greatindiancompany/.github` is the public GitHub organization meta repository for Great Indian Company. It is not a product codebase.

It does two jobs:

1. Organization profile. `profile/README.md` is what GitHub renders on the public organization page.
2. Community health defaults. Files here can apply to other repositories in the `greatindiancompany` organization when those repositories do not already contain their own copy. GitHub documents that behavior as default community health files. A license file is not one of those defaults.

As of the 2026-09-23 review, the other public repositories in this organization (`greatindiancompany`, `inspir-landing`, `ai-learning-platform`, `ai-study-platform`) each already have their own `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`, and `LICENSE`. Editing those files here does not change those copies. `ai-study-platform` has no `.github` directory, so it can still inherit issue and pull request templates from this repo.

This repository is documentation and profile copy. It has no application runtime, no GitHub Actions workflows, and no documented deploy step.

## Owner and scope

This repo is the GIC entity and brand lane: the organization profile, community health files, and how the GitHub organization describes itself.

Shopify product engineering and go-to-market are out of scope. Do not open, edit, or review `mark-*` product repositories as part of work in this repo. The organization profile links to Shopify App Store listings. Those links are not permission to change those products from here.

## What the files mean

- `profile/README.md` — public organization profile. This is the page visitors read on the organization, not the repository README.
- `README.md` — README for this repository. It describes the profile repo. It is not the organization profile.
- `SECURITY.md` — security policy for this repository, and the default for any repository that does not have its own. It says not to open a public issue for vulnerabilities, and to contact the repository owner privately with a summary, reproduction steps, the affected surface, redacted evidence, and believed impact. It does not name an email address, a form, or a response window. `.github/ISSUE_TEMPLATE/config.yml` points security reports at GitHub Security Advisories for this repository. This file does not say whether private vulnerability reporting is turned on.
- `CONTRIBUTING.md` — contribution guide. The steps written in the file are: edit `profile/README.md`, commit to `main`, then review the rendered organization profile after pushing. A pull request template also exists at `.github/pull_request_template.md`. The guide does not name a required reviewer.
- `CODE_OF_CONDUCT.md` — custom conduct expectations (respectful disagreement, specific feedback, privacy, no harassment). Enforcement text says maintainers may remove comments, close issues, block users, or reject contributions, and that reports go to the repository owner privately. No contact address is written in the file.
- `LICENSE` — MIT License, Copyright (c) 2026 Great Indian Company. It covers this repository. GitHub does not copy it onto other repositories as a default license.
- `.github/ISSUE_TEMPLATE/` — bug report, feature request, and a contact link for security reports.
- `.github/pull_request_template.md` — asks for what changed, why, and how it was tested.
- `ORG_META_REVIEW.md` — point-in-time review from 2026-09-23. It records findings. It is not an operating process, and it does not authorize follow-up edits by itself.

## Safety

- Do not commit secrets, tokens, credentials, env files, production data, or private user content.
- Open pull requests as drafts. Do not merge. An agent does not merge this repository; the founder does.
- Do not invite collaborators. Do not invite `cursoragent` or any other agent account.
- Do not invent contribution, security, support, or release processes that are not written in this repo. If a file is silent, say so.
- Stay inside this repository unless a task explicitly names another repo. `mark-*` product repositories stay out of scope even then.
