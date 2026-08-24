# LipDev Python Backend GitHub Profile Design

**Date:** August 24, 2026
**Repository:** `LipDev-sudo/LipDev-sudo`
**Target branch:** `feat/python-backend-profile`

## Objective

Replace the current frontend-focused GitHub profile README with an English-first,
recruiter-oriented profile for Python backend and automation opportunities. The
profile must present offensive security as a complementary learning path, not as
professional expertise.

The implementation must be visually inspired by the approved references while
remaining original. It will use a dark editorial layout, restrained purple
lighting, compact technology badges, live GitHub statistics, a custom illustrated
portrait, and a transparent animated Gengar accent.

## Truth and Positioning Rules

The public GitHub account currently contains TypeScript/frontend repositories and
does not contain a public Python project. The README must not imply otherwise.

- Primary title: `Aspiring Python Backend Developer`
- Complementary title: `Cybersecurity Enthusiast`
- Additional focus: Python automation
- Do not claim paid Python work, production backend experience, completed security
  projects, vulnerability-discovery results, certifications, or advanced English.
- Do not use `Freelance Python Backend Developer`.
- Do not label Hamilton as a penetration tester, security researcher, ethical
  hacker, cybersecurity specialist, or expert.
- Flask may be presented as the Python framework with the most current hands-on
  practice.
- FastAPI, Burp Suite, and TryHackMe must be visibly presented as learning areas.
- `pytest` may be listed under tools/practice, but the README must not claim tested
  production projects because no surviving public project demonstrates that.
- Docker, Linux, SQLite, MySQL, Selenium, Requests, Git, and GitHub may be listed as
  tools Hamilton reports using in practice.
- Parrot OS may be described as the daily Linux environment.
- Nmap may be described only in the context of authorized labs.

## Approved Personal Information

- Display name: Hamilton Felipe
- Banner brand: LipDev
- Location: Recife, Pernambuco, Brazil
- Availability: remote, hybrid, and on-site junior opportunities
- Public email: `hamiltonfelipe019@gmail.com`
- LinkedIn: `https://www.linkedin.com/in/hamilton-felipe-875054383/`
- GitHub: `https://github.com/LipDev-sudo`
- Education: Systems Analysis and Development, Centro Universitário Maurício de
  Nassau, started April 2024, expected completion March 2027
- English level: basic; omit from the main README because it does not strengthen
  the positioning and the profile is already written in English

Instagram and the frontend portfolio link must be removed from the profile README.

## README Information Architecture

### 1. Banner

Use a repository-hosted horizontal image with a near-black background and restrained
purple lighting. It must contain:

- `LipDev`
- `You don't need to be good to start, but you need to start to become good.`
- `Não precisa ser bom para começar, mas precisa começar para ser bom.`

The English line must be visually primary and the Portuguese line secondary.

### 2. Professional Identity

Present Hamilton Felipe with this hierarchy:

1. `Aspiring Python Backend Developer`
2. `Cybersecurity Enthusiast`
3. Python automation, REST APIs, SQLite/MySQL, and Git-based workflows
4. Recife location and opportunity availability

The section will include a repository-hosted illustrated portrait derived from
Hamilton's existing portfolio photo. The approved style uses editorial line work,
a nearly black background, and purple rim lighting. It must remain recognizable and
professional rather than looking like a generic generated avatar.

### 3. Contact Actions

Use compact, accessible badges for LinkedIn, email, and GitHub. Each badge must have
descriptive alternative text and a verified URL. Do not include Instagram or the
frontend portfolio.

### 4. Technology Groups

Keep the badges compact and grouped by actual level:

- **Backend and data:** Python, Flask, REST APIs, SQLite, MySQL
- **Automation:** Selenium, Requests, system automation, terminal tools
- **Tools and quality:** pytest, Docker, Git, GitHub, Linux/Parrot OS
- **Currently learning:** FastAPI, API security, OWASP fundamentals, Nmap in
  authorized labs, Burp Suite, TryHackMe

Do not list frontend technologies in the main technology section. Do not present
authentication, JWT, SQLAlchemy, Pydantic, Swagger/OpenAPI, or automated test
coverage as existing competencies because the discovery did not substantiate them.

### 5. Live GitHub Statistics

Use dynamic public widgets tied directly to the `LipDev-sudo` username:

- a live contribution activity graph with a dark purple theme;
- a compact general statistics card.

Do not use hand-authored numbers or a static graph. Avoid a language-ranking card
because the current public history is frontend-heavy and would conflict with the
new career direction. Each widget endpoint must return a valid image during final
verification. If a candidate endpoint is unavailable or unstable, omit it rather
than leaving a broken image.

### 6. About Me

Use concise, natural English. Explain that Hamilton is transitioning his public work
toward Python backend and automation, practices Flask and REST APIs, works with
SQLite/MySQL, and is developing security-conscious habits. Mention the degree and
expected completion date in one sentence. Do not claim professional Python tenure.

### 7. Featured Project: Odin

Odin is the only featured future-facing project. Label it clearly as
`Planning / Early Prototype`.

Describe only the intended objective: a terminal-oriented assistant intended to
help inspect a supplied web application URL and organize potential security findings
for authorized testing. State that the current prototype is not functional. Do not
claim that it discovers vulnerabilities, uses AI successfully, performs autonomous
testing, or is production-ready. Do not add a GitHub link until a public repository
exists.

### 8. Goals

List concrete next steps rather than generic ambition:

- publish a maintainable Python REST API;
- add input validation, authentication, error handling, logging, documentation, and
  automated tests;
- publish a useful Python automation project;
- progress through authorized offensive-security labs;
- turn Odin from a plan into a safe, testable prototype.

### 9. Footer Accent

Use the user-supplied 500 x 493 animated Gengar GIF. Inspection confirmed 20 frames,
an infinite loop, and an existing transparent palette entry, so no background-removal
edit is required. Keep the accent small enough that it does not dominate the profile
or create a stereotypical hacker presentation.

## Visual System

- Background inside custom images: near-black (`#08090f` family)
- Primary accent: purple (`#8b5cf6` / `#9d6be0` family)
- Secondary accent: muted lavender
- Text inside images: off-white with accessible contrast
- Layout: centered editorial sections, compact badges, generous spacing
- No Matrix rain, neon overload, fake terminals, skulls, threat claims, or clutter
- GitHub light mode must remain readable because the custom banner and portrait carry
  their own backgrounds

## Repository Changes

Expected implementation files:

- `README.md`
- `assets/lipdev-banner.png`
- `assets/hamilton-purple-portrait.png`
- `assets/gengar.gif`
- `AGENTS.md`
- this design and the subsequent implementation plan under `docs/superpowers/`

No package manager, runtime dependency, website, deployment, GitHub visibility,
authentication setting, or production data is involved.

## Repository Cleanup Review

The separate request to review old repositories is read-only in this delivery.
Produce a recommendation table with `keep`, `archive`, or `consider deletion` and a
reason for each repository. Do not archive, delete, rename, transfer, or change the
visibility of any repository. The `Portifolio` repository may be marked
`consider deletion after backup`, with essential data identified before any future
destructive action.

## Validation

Before delivery:

1. Render or preview the README at desktop and narrow/mobile widths.
2. Confirm the banner, portrait, and GIF render from repository-relative paths.
3. Confirm the Gengar GIF remains animated and transparent.
4. Confirm each external contact link resolves correctly.
5. Confirm each statistics endpoint returns a valid image.
6. Search the final README for Portuguese text outside the approved banner quote.
7. Search for obsolete frontend positioning, frontend service offers, Instagram, and
   the old frontend portfolio link.
8. Search for unsupported claims such as professional Python experience, completed
   Odin functionality, security expertise, certifications, or vulnerability results.
9. Run a filename-only secret scan without printing secret values.
10. Run `git diff --check` and verify a clean working tree after commits.

The repository has no application code, package manifest, lint script, typecheck,
tests, or production build. Those commands are therefore not applicable.

## Delivery

Use small descriptive commits, push only the feature branch, and open one pull
request targeting `main`. Do not merge. Report the branch, commits, changed files,
validation evidence, PR URL, cleanup recommendations, and any remaining user action.
