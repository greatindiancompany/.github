# Organization meta review

Point-in-time review of `greatindiancompany/.github` on 2026-09-23. Read-only against the rest of the organization. No product repositories were changed. Shopify `mark-*` repositories were not opened.

Sources checked:

- This repo: `profile/README.md`, `README.md`, `SECURITY.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `LICENSE`, `.github/ISSUE_TEMPLATE/`, `.github/pull_request_template.md`.
- GitHub organization `greatindiancompany` (public metadata and the five public repositories).
- Brand lander source in `greatindiancompany` (`src/pages/index.astro`, `src/layouts/Layout.astro`) and the live apex response at `https://greatindiancompany.com`.

## What the profile asserts

`profile/README.md` is the organization profile. It leads with "Applied AI from India for the world." It places the company in Bengaluru, Dubai, London, and California, and calls Great Indian Company one of India's earliest applied-AI product labs, building on GPT-3 since September 2022.

It links the website, X (`@greatindianco`), LinkedIn, Instagram (`instagram.com/greatindiancompany`), and Facebook. Badges name applied AI, India, Shopify, Astro, React, and Node.js.

The "Start here" and "Repos" sections list four public repositories (`greatindiancompany`, `inspir-landing`, `ai-learning-platform`, `ai-study-platform`) and two Shopify App Store listings (Mark Delivered, Mark Shipping Status). Those four repository names match the public organization listing aside from this `.github` repo. The App Store listings are not GitHub repositories in this organization. The profile says more commerce tooling will be linked when it is clean enough to expose.

"Shipped lore" asserts pre-ChatGPT GPT-3 apps, 15+ AI products with Product Hunt top-10 launches, Pet Dukaan (100,000+ users, roughly $500K revenue, acquired by Roms N Raks), and Inspir as a quiz community becoming an AI learning platform.

The philosophy section says the name is an assertion and that the company is building for the Indian century, with India as the default context and the world as the default market.

The repository `README.md` (not the org profile) restates a shorter mission: applied AI from India for the world, practical software, commerce tooling, and learning products. It says this repo is documentation-only and that contributions are welcome across docs, accessibility, tests, bugs, UI polish, data validation, and safer AI behavior.

## 1. Consistency with the brand lander thesis

The live lander at `https://greatindiancompany.com` (HTTP 200 on this date) and `src/pages/index.astro` use one sentence:

> great indian company isn't just a name; it's our assertion to the world. we are building the great indian century!

`src/layouts/Layout.astro` sets the meta description and Open Graph description to "Bringing India to the World". The canonical URL is `https://greatindiancompany.com` (no `www`). Social links on the page are Instagram `instagram.com/greatindianco`, `mailto:hello@greatindiancompany.com`, X `@greatindianco`, and LinkedIn `linkedin.com/company/greatindiancompany`. There is no Facebook link, no city list, no product catalog, and no Shopify mention on that page.

The GitHub organization description is "building the great indian century!" The organization website field is `https://www.greatindiancompany.com`. The organization email field is `devrel@greatindiancompany.com`. The X username is `greatindianco`. The organization was created on 2026-05-26. That date is the GitHub organization's creation date, not a claim about when the company started.

Where the surfaces agree:

- The name-as-assertion line in the profile philosophy tracks the lander headline.
- "Indian century" / "great indian century" is the shared thesis.
- X and LinkedIn URLs match.
- "From India for the world" on the profile is in the same direction as "Bringing India to the World", but it is not the same sentence.

Where they diverge:

- The lander is a single assertion. The profile is a product and history index (applied-AI lab, learning repos, Shopify apps, revenue and acquisition figures). None of those catalog claims appear on the lander page.
- The profile's primary website links use `https://www.greatindiancompany.com`. On this date `www` had no A record and a single AAAA of `100::` (the IPv6 discard prefix). Connections to `www` failed. The apex host answered and served the lander. The lander's own canonical URL is the apex host.
- Instagram: lander uses `/greatindianco` (same handle as X). The profile uses `/greatindiancompany`. Unauthenticated requests to both Instagram URLs redirected to a login wall, so this review does not prove which profile is live. The strings disagree.
- Email: lander uses `hello@greatindiancompany.com`. The organization profile email is `devrel@greatindiancompany.com`. `SECURITY.md` and `CODE_OF_CONDUCT.md` name neither.
- The profile adds Facebook and four cities. The lander page does not.
- The profile's Pet Dukaan, Product Hunt, user, and revenue figures are only in the profile. This review did not verify them and does not treat them as false. They are not on the lander.

The root `README.md` mission sits between the two: applied AI, commerce tooling, and learning products, without the lander's exact assertion sentence and without the profile's numerical lore.

## 2. SECURITY.md and the disclosure path

`SECURITY.md` tells reporters not to open a public issue, and to contact the repository owner privately with a summary, reproduction steps, affected route or workflow, redacted screenshots or logs, and believed impact. Supported versions are "the current default branch unless maintainers announce a release policy."

What is missing from the file:

- No email, no `mailto`, no security form, and no named owner.
- No statement of whether GitHub private vulnerability reporting is enabled.
- No response-time commitment. None is documented elsewhere in this repo, so this review does not invent one.

`.github/ISSUE_TEMPLATE/config.yml` adds a contact link to `https://github.com/greatindiancompany/.github/security/advisories/new`. The security-advisories list for this repository returned an empty list. A check of the vulnerability-alerts API returned 403 for this token, so private reporting could not be confirmed on or off.

`CODE_OF_CONDUCT.md` has the same gap: reports go to "the repository owner privately," with no address.

The policy text itself is generic product language (auth bypass, admin routes, provider keys, prompt or tool leaks, cross-user data). That does not match this documentation-only repo. It still matters, because a repository without its own `SECURITY.md` inherits this file. The four other public repositories already ship their own `SECURITY.md`, so they do not inherit this copy today. A new public repository would.

## 3. Automation under `.github/`

Present:

- `.github/ISSUE_TEMPLATE/bug_report.md`
- `.github/ISSUE_TEMPLATE/feature_request.md`
- `.github/ISSUE_TEMPLATE/config.yml` (`blank_issues_enabled: true`, plus the security advisories link)
- `.github/pull_request_template.md`

Absent in this repository:

- GitHub Actions workflows (Actions workflow count is 0).
- Dependabot config.
- `CODEOWNERS`.
- Any documented CI command. `README.md` and `CONTRIBUTING.md` both say the check is "Review the rendered organization profile after pushing."

The same absence showed up on the other public repositories checked on this date: `greatindiancompany`, `inspir-landing`, and `ai-learning-platform` each have issue and pull request templates and zero workflows. `ai-study-platform` has no `.github` directory and zero workflows, so it inherits templates from this repo.

`CONTRIBUTING.md` tells contributors to commit to `main`. The pull request template assumes a review. The two are not aligned, and nothing in the repo says which one wins. There is no branch protection rule recorded in these files.

Issue templates assume a product UI ("Go to / Click / Type", screenshots, device, browser). That shape is a poor fit for edits to `profile/README.md`. Labels `bug` and `enhancement` exist on this repository. GitHub's default-template docs say a template label must also exist on each repository that uses the template. This review did not audit labels on the other repositories.

The community profile API for this repo reported `health_percentage` 87, `description` null, `files.issue_template` null, and a detected pull request template. The issue-template directory is still on `main`, so the null API field does not mean the files are absent. GitHub's community checklist is eight items (description, README, code of conduct, contributing, license, security policy, issue templates, pull request template). 87 is one item short of 100. The repository description is the item this review could confirm is empty.

## 4. Licensing and community health

- `LICENSE` is MIT, Copyright (c) 2026 Great Indian Company. It is a normal MIT text.
- GitHub does not publish a default license from a `.github` repository. Each repository needs its own. The four other public repositories already include an MIT `LICENSE`.
- `CODE_OF_CONDUCT.md` is custom. The community profile reports it as "Other", not a recognized covenant text. Enforcement contact is unspecified.
- `CONTRIBUTING.md` and the root `README.md` read like a product repo: screenshots for UI changes, tests, accessibility, deployment hygiene, "run the checks." The only check written down is a manual look at the rendered profile after a push. There is no test suite in this repo.
- No `SUPPORT.md`. No `FUNDING.yml`. No `GOVERNANCE.md`. Nothing in the repo says those were intended.
- Repository description and homepage on the `.github` repo are empty. Topics are empty. The wiki is enabled. Discussions are off. Issues are on.
- Community health files at the root of this repo are valid default locations for code of conduct, contributing, and security policy. They do not override the copies already committed in the other public repositories.

## Prioritized recommendations

Document only. This pull request does not apply them, except for adding `AGENTS.md` and this file.

### P0

None. This review did not find secrets in the tree, a broken license text, or a public vulnerability report. The gaps below are real and should be fixed by the founder. They are not an active exposure in this repository.

### P1

1. Fix the organization profile website URL. `profile/README.md` links `https://www.greatindiancompany.com` in the header and the footer. On 2026-09-23 that host had no A record and AAAA `100::`, and it did not connect. `https://greatindiancompany.com` returned the lander. The organization website field uses the same `www` host. Change the links only after the founder picks the canonical host, or restore `www` in DNS. Do not leave the profile pointing at the discard address.
2. Decide the profile's first screen against the lander thesis before adding more catalog copy. The lander's public sentence is the great-indian-century assertion, with meta copy "Bringing India to the World." The profile leads with an applied-AI lab, Shopify, and shipped-lore numbers the lander does not state. Founder should confirm or cut the Pet Dukaan figures, the acquisition line, the Product Hunt claim, the September 2022 date, the city list, and the Shopify badges. This review does not treat those lines as disproven.
3. Put one private contact in `SECURITY.md` and `CODE_OF_CONDUCT.md`. The lander publishes `hello@greatindiancompany.com`. The organization email field is `devrel@greatindiancompany.com`. Neither file names an address. Founder should pick the mailbox, then confirm whether GitHub private vulnerability reporting is enabled for the advisories URL already linked from `config.yml`.
4. Make the Instagram handle agree with the lander. Lander and the X account use `greatindianco`. The profile uses `instagram.com/greatindiancompany`.

### P2

1. Rewrite the "commit changes to main" blocks in `README.md` and `CONTRIBUTING.md` so they match the pull request template, or delete the template if direct commits to `main` are actually the rule. The files currently describe both.
2. Replace product boilerplate in `README.md` and `CONTRIBUTING.md` (tests, UI polish, deployment, accessibility) with instructions for a documentation-only profile repo. The quality check can stay manual until someone adds a real one.
3. Set a repository description on `.github`. The community profile description is null, and the health score is 87.
4. Add automation only if the founder wants it. There is no workflow, Dependabot config, or `CODEOWNERS` in this repo. A link check would have caught the `www` host. Do not add organization-wide Actions from this review.
5. If a recognized code of conduct is wanted, replace the custom file explicitly. Today GitHub classifies it as "Other." `SUPPORT.md` is absent; add one only if there is a real support channel.
6. Narrow the default issue templates, or accept that `ai-study-platform` (no `.github` directory) inherits the current UI-shaped bug template. Confirm `bug` and `enhancement` labels exist on repositories that inherit these templates.
7. Keep Shopify App Store links out of agent work on this repo. Mark Delivered and Mark Shipping Status are listings, not public repositories in this organization. `mark-*` product repos stay out of scope.

## Out of scope for this review

- No edits to `greatindiancompany`, `inspir-landing`, `ai-learning-platform`, `ai-study-platform`, or any `mark-*` repository.
- No collaborator invites.
- No merge.
