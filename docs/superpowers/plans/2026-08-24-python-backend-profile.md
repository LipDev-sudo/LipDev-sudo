# LipDev Python Backend GitHub Profile Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the frontend-focused GitHub profile with an honest, visually distinctive Python backend, automation, and cybersecurity-learning profile.

**Architecture:** Keep the repository static and dependency-free: one GitHub-rendered `README.md`, three repository-hosted visual assets, and one read-only repository cleanup report. Dynamic statistics are embedded from public GitHub profile-card services and validated before delivery; no application runtime or build system is introduced.

**Tech Stack:** GitHub Flavored Markdown, HTML-in-Markdown, Shields.io, GitHub profile summary cards, GitHub activity graph, PNG, animated GIF, Git, GitHub CLI

**Spec:** `docs/superpowers/specs/2026-08-24-python-backend-profile-design.md`

## Global Constraints

- Work only in `LipDev-sudo/LipDev-sudo` on branch `feat/python-backend-profile`.
- Never push directly to `main`, change repository visibility, merge, archive, or delete a repository.
- Preserve the existing draft PR #1 without modification.
- Do not add package managers, runtime dependencies, Actions secrets, or deployment configuration.
- Present `Aspiring Python Backend Developer` as the primary title and `Cybersecurity Enthusiast` as the complementary title.
- Do not claim paid Python work, professional Python tenure, production backend experience, completed security projects, certifications, vulnerability results, or advanced English.
- Present Odin as `Planning / Early Prototype` and explicitly state that the current prototype is not functional.
- Keep the README English-first; the only required Portuguese content is the secondary banner quote.
- Remove Instagram, the frontend portfolio link, frontend service offers, and frontend technology positioning from the README.
- Use real, live statistics tied to `LipDev-sudo`; never use static or invented values.
- Do not delete, archive, rename, transfer, or change the visibility of any repository during the cleanup review.

---

### Task 1: Produce and stage the approved visual assets

**Files:**
- Create: `assets/lipdev-banner.png`
- Create: `assets/hamilton-purple-portrait.png`
- Create: `assets/gengar.gif`

**Interfaces:**
- Consumes: the source portrait at `Portifolio/public/images/felipe.jpeg`, the approved art reference supplied in the conversation, and `C:\Users\Felipe\Downloads\gif`
- Produces: stable repository-relative image paths consumed by `README.md`

- [ ] **Step 1: Inspect the source files before editing**

Run:

```powershell
Get-Item 'C:\Users\Felipe\Documents\Codex\2026-07-24\agent-1-portfolio\work\Portifolio\public\images\felipe.jpeg'
Get-Item 'C:\Users\Felipe\Downloads\gif'
```

Expected: both files exist; the GIF is 166,968 bytes before copying.

- [ ] **Step 2: Generate the portrait using the image-generation skill**

Use the existing portrait as the identity reference and the approved editorial illustration as the style reference. Use this prompt:

```text
Create a square professional illustrated portrait of the same adult man in the identity reference. Preserve his recognizable facial structure, glasses, short dark hair, beard, skin tone, and calm expression. Use expressive editorial line work and angular painted shading inspired by the supplied art reference, without copying its subject. Background almost black, subtle purple rim lighting and violet reflections, centered head and shoulders, dark simple clothing, polished technology-profile avatar, high contrast, no text, no logos, no cyberpunk clutter, no hacker symbols, no neon overload.
```

Save the selected result as `assets/hamilton-purple-portrait.png` at a square resolution of at least 1024 x 1024.

- [ ] **Step 3: Generate the banner using the image-generation skill**

Use this prompt:

```text
Create a wide 1600 x 420 GitHub profile banner with a near-black editorial technology aesthetic and restrained purple lighting. Abstract layered shapes should subtly suggest backend systems, API routes, terminal workflows, and data connections without literal code screenshots. Leave generous centered negative space for typography. Include exactly the brand text “LipDev”. Below it include exactly “You don't need to be good to start, but you need to start to become good.” and, smaller, “Não precisa ser bom para começar, mas precisa começar para ser bom.” Use off-white and muted lavender text with excellent contrast. No Matrix rain, no skulls, no locks, no stock hacker imagery, no excessive neon, no third-party logos.
```

Save the selected result as `assets/lipdev-banner.png`.

- [ ] **Step 4: Copy the user-supplied transparent animation without recompression**

Run a byte-preserving copy from `C:\Users\Felipe\Downloads\gif` to `assets/gengar.gif`. Do not convert it to PNG or re-encode it.

- [ ] **Step 5: Validate all asset formats and dimensions**

Use Pillow to print only format, dimensions, frame count, transparency metadata, and file size. Expected:

- banner: PNG, wide landscape ratio;
- portrait: PNG, square, at least 1024 x 1024;
- Gengar: GIF, 500 x 493, 20 frames, loop `0`, transparency entry present, 166,968 bytes.

- [ ] **Step 6: Inspect the latest banner, portrait, and representative GIF frame visually**

Reject any asset with distorted identity, clipped text, misspelled quotes, low contrast, white GIF background, or generic hacker imagery. Regenerate only the failing asset and repeat Step 5.

- [ ] **Step 7: Commit the approved assets**

```bash
git add assets/lipdev-banner.png assets/hamilton-purple-portrait.png assets/gengar.gif
git commit -m "feat: add Python backend profile artwork"
```

---

### Task 2: Rewrite the GitHub profile README

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: `assets/lipdev-banner.png`, `assets/hamilton-purple-portrait.png`, `assets/gengar.gif`
- Produces: the complete profile rendered by GitHub at `https://github.com/LipDev-sudo`

- [ ] **Step 1: Replace the old README with the approved information hierarchy**

Use the following content as the implementation baseline. Keep line wrapping readable and use repository-relative asset paths.

```markdown
<p align="center">
  <img src="assets/lipdev-banner.png" alt="LipDev — Python backend, automation, and continuous learning" width="100%" />
</p>

<table>
  <tr>
    <td width="30%" align="center" valign="top">
      <img src="assets/hamilton-purple-portrait.png" alt="Illustrated portrait of Hamilton Felipe" width="220" />
    </td>
    <td width="70%" valign="middle">
      <h1>Hamilton Felipe</h1>
      <h3>Aspiring Python Backend Developer · Cybersecurity Enthusiast</h3>
      <p>Python automation · REST APIs · SQLite · MySQL · Git</p>
      <p>📍 Recife, Pernambuco, Brazil</p>
      <p>Open to remote, hybrid, and on-site junior opportunities.</p>
    </td>
  </tr>
</table>

<p align="center">
  <a href="https://www.linkedin.com/in/hamilton-felipe-875054383/"><img src="https://img.shields.io/badge/LinkedIn-6D28D9?style=for-the-badge&logo=linkedin&logoColor=white" alt="Hamilton Felipe on LinkedIn" /></a>
  <a href="mailto:hamiltonfelipe019@gmail.com"><img src="https://img.shields.io/badge/Email-4C1D95?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Hamilton Felipe" /></a>
  <a href="https://github.com/LipDev-sudo"><img src="https://img.shields.io/badge/GitHub-17131F?style=for-the-badge&logo=github&logoColor=white" alt="LipDev-sudo on GitHub" /></a>
</p>

---

## ⚙️ Technologies

### Backend and data

![Python](https://img.shields.io/badge/Python-17131F?style=flat-square&logo=python&logoColor=B794F4)
![Flask](https://img.shields.io/badge/Flask-17131F?style=flat-square&logo=flask&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST_APIs-17131F?style=flat-square&logo=postman&logoColor=B794F4)
![SQLite](https://img.shields.io/badge/SQLite-17131F?style=flat-square&logo=sqlite&logoColor=B794F4)
![MySQL](https://img.shields.io/badge/MySQL-17131F?style=flat-square&logo=mysql&logoColor=B794F4)

### Automation and workflow

![Selenium](https://img.shields.io/badge/Selenium-17131F?style=flat-square&logo=selenium&logoColor=B794F4)
![Requests](https://img.shields.io/badge/Requests-17131F?style=flat-square&logo=python&logoColor=B794F4)
![Docker](https://img.shields.io/badge/Docker-17131F?style=flat-square&logo=docker&logoColor=B794F4)
![pytest](https://img.shields.io/badge/pytest-17131F?style=flat-square&logo=pytest&logoColor=B794F4)
![Git](https://img.shields.io/badge/Git-17131F?style=flat-square&logo=git&logoColor=B794F4)
![GitHub](https://img.shields.io/badge/GitHub-17131F?style=flat-square&logo=github&logoColor=white)
![Parrot OS](https://img.shields.io/badge/Parrot_OS-17131F?style=flat-square&logo=linux&logoColor=B794F4)

### Currently learning

`FastAPI` · `API security` · `OWASP fundamentals` · `Nmap in authorized labs` · `Burp Suite` · `TryHackMe`

---

## 📊 Live GitHub Statistics

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=LipDev-sudo&theme=tokyonight" alt="Live GitHub statistics for LipDev-sudo" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=LipDev-sudo&bg_color=08090f&color=cab8ed&line=8b5cf6&point=ffffff&area=true&hide_border=true" alt="Live GitHub contribution activity graph for LipDev-sudo" width="100%" />
</p>

---

## 👨‍💻 About Me

I am transitioning my public work toward Python backend development and automation. My current practice includes building Flask routes and CRUD flows, working with REST APIs, SQLite and MySQL, and creating Python automations with Selenium and Requests.

Security is a complementary part of my learning path. I use Parrot OS as my daily Linux environment and study offensive-security fundamentals through authorized labs, with current exposure to Nmap and early familiarization with Burp Suite and TryHackMe.

I am pursuing a degree in Systems Analysis and Development at Centro Universitário Maurício de Nassau, started in April 2024, with expected completion in March 2027.

---

## 🔭 Featured Project — Odin

**Status: Planning / Early Prototype**

Odin is a planned terminal-oriented assistant for authorized web-application security study. Its intended goal is to receive a target URL, organize observations, and help structure potential findings for manual review.

The current prototype is not functional yet. The project does not claim automated vulnerability detection, autonomous testing, or production readiness.

---

## 🎯 Goals

- Publish a maintainable Python REST API.
- Add input validation, authentication, error handling, logging, documentation, and automated tests.
- Publish a useful Python automation project.
- Progress through authorized offensive-security labs.
- Turn Odin into a safe and testable prototype.

<p align="center">
  <img src="assets/gengar.gif" alt="Animated Gengar" width="180" />
</p>

<p align="center"><em>Start, learn, improve, and keep building.</em></p>
```

- [ ] **Step 2: Run positioning and unsupported-claim scans**

Run case-insensitive searches over `README.md` for:

```text
React|Next.js|TypeScript|Tailwind|frontend|web design|landing page|e-commerce|Instagram|lipdev.vercel.app|Freelance Python|penetration tester|security expert|certified|production-ready|detects vulnerabilities
```

Expected: zero matches except the explicit sentence denying production readiness if the scan is run before that phrase is refined. Adjust the scan to assert that no affirmative unsupported claim remains.

- [ ] **Step 3: Validate approved personal data and learning labels**

Confirm exact matches for:

```text
Aspiring Python Backend Developer
Cybersecurity Enthusiast
Recife, Pernambuco, Brazil
Planning / Early Prototype
The current prototype is not functional yet.
expected completion in March 2027
Currently learning
```

- [ ] **Step 4: Commit the README rewrite**

```bash
git add README.md
git commit -m "feat: reposition profile for Python backend"
```

---

### Task 3: Audit dynamic widgets, links, and responsive rendering

**Files:**
- Modify: `README.md` only if validation finds a broken widget or layout issue

**Interfaces:**
- Consumes: the completed README and public external endpoints
- Produces: a README with verified live links, images, and narrow-width behavior

- [ ] **Step 1: Verify contact links without triggering messages**

Use HEAD/GET requests with redirects enabled for GitHub and LinkedIn. Validate the email address syntactically without sending mail. Expected: GitHub resolves successfully; LinkedIn may block automation, in which case confirm the existing public URL format and record the limitation.

- [ ] **Step 2: Verify dynamic image endpoints**

Request the summary-card and activity-graph URLs. Require HTTP 200 and an image content type. If either fails twice, separated by a normal retry, remove only the failing widget from `README.md` and keep the stable one.

- [ ] **Step 3: Preview GitHub Flavored Markdown locally or in a safe branch preview**

Inspect desktop and narrow/mobile widths. Confirm:

- banner text is legible and not clipped;
- the identity table stacks or remains readable at narrow width;
- badges wrap without horizontal overflow;
- statistics scale to the content width;
- portrait and Gengar do not dominate the page;
- light and dark GitHub themes retain readable custom images.

- [ ] **Step 4: Re-run content scans and whitespace validation**

Run `git diff --check` and the searches from Task 2. Confirm no obsolete frontend positioning or unsupported security claim was introduced during layout fixes.

- [ ] **Step 5: Commit validation-driven corrections if required**

If no file changed, do not create an empty commit. If corrections were needed:

```bash
git add README.md
git commit -m "fix: harden profile rendering and live widgets"
```

---

### Task 4: Produce the non-destructive repository cleanup recommendation

**Files:**
- Create: `docs/repository-cleanup-review.md`

**Interfaces:**
- Consumes: live read-only GitHub repository metadata, README files, default branches, activity dates, visibility, and verified deployment URLs
- Produces: a recommendation only; no repository mutation

- [ ] **Step 1: Inventory every repository owned by LipDev-sudo**

Use `gh repo list LipDev-sudo --limit 100` and read-only API calls. Record repository name, visibility, archived state, primary language, last push date, description, homepage, and whether the default branch contains substantive source code.

- [ ] **Step 2: Classify each repository using explicit criteria**

Use exactly these labels:

- `KEEP`: supports the backend/automation/security direction, contains unique evidence, or is required for the GitHub profile;
- `ARCHIVE`: useful historical work that should remain accessible but is no longer an active direction;
- `CONSIDER DELETION AFTER BACKUP`: duplicate, empty, abandoned, or misleading work with no unique evidence or active dependency.

Do not classify any repository only from its name. Inspect its default branch and links first.

- [ ] **Step 3: Identify essential data before recommending deletion**

For every `CONSIDER DELETION AFTER BACKUP` row, list what must be preserved: source history, screenshots, documents, environment-variable names without values, deployment URLs, or reusable assets. For `Portifolio`, explicitly identify the resume PDF, contact details, image assets, project link inventory, and any unique API/contact implementation before recommending future removal.

- [ ] **Step 4: Write the report with a destructive-action warning**

The report must begin with:

```markdown
# Repository Cleanup Review

This is a read-only recommendation. No repository was archived, deleted, renamed, transferred, or made private. Any destructive action requires a separate explicit confirmation after backup targets are reviewed.
```

Include one row per repository and a final ordered cleanup proposal. Do not include secret values.

- [ ] **Step 5: Commit the review**

```bash
git add docs/repository-cleanup-review.md
git commit -m "docs: review repositories for backend transition"
```

---

### Task 5: Final verification, push, and pull request

**Files:**
- Modify: only files already in scope if final verification finds a defect

**Interfaces:**
- Consumes: all committed assets, README, spec, plan, and cleanup review
- Produces: one reviewable branch and one pull request; no merge

- [ ] **Step 1: Run the final repository checks**

Run:

```powershell
git status --short --branch
git diff --check origin/main...HEAD
git diff --name-status origin/main...HEAD
```

Expected: only `AGENTS.md`, `README.md`, the three assets, the spec, the plan, and the cleanup review are changed.

- [ ] **Step 2: Run a filename-only secret scan**

Search tracked text files for strong AWS, GitHub, OpenAI, private-key, and password-assignment patterns. Print only filenames containing candidates, never matching values. Expected: zero candidate files.

- [ ] **Step 3: Confirm non-applicable application checks**

Verify that the repository contains no `package.json`, Python project manifest, application source, lint configuration, test suite, or build command. Record lint, typecheck, tests, build, and dependency audit as not applicable rather than inventing results.

- [ ] **Step 4: Push only the feature branch**

```bash
git push -u origin feat/python-backend-profile
```

- [ ] **Step 5: Open one pull request against main**

Use title:

```text
feat: reposition profile for Python backend
```

The PR body must summarize the honest positioning, original purple artwork, live statistics, Odin status, validation, and read-only cleanup report. It must explicitly state that PR #1 was not modified and no repository was deleted or archived.

- [ ] **Step 6: Verify the GitHub-rendered branch and PR checks**

Open the branch README and PR. Recheck images, responsive layout, links, live statistics, and text after GitHub rendering. Record the PR URL. Do not merge.

- [ ] **Step 7: Deliver the final evidence**

Report:

- branch and commits;
- changed files;
- visual and content decisions;
- live-widget and link results;
- desktop/mobile review result;
- lint/typecheck/tests/build/audit as not applicable;
- cleanup recommendation path;
- PR URL;
- required user actions, including review/merge and any future separately approved repository cleanup.
