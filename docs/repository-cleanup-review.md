# Repository Cleanup Review

**Date:** August 24, 2026
**Scope:** Read-only review of repositories visible to the authenticated owner account

No repository was archived, deleted, renamed, transferred, made public, or made
private during this review. Recommendations are based on repository metadata,
default-branch file trees, READMEs, package manifests, and branch names.

## Recommendation summary

| Repository | Visibility | Recommendation | Evidence and reason |
| --- | --- | --- | --- |
| `LipDev-sudo` | Public | **KEEP** | GitHub profile repository. This branch turns it into the primary recruiting surface for Python backend, automation, and security learning. |
| `Code-Farming` | Private | **KEEP** | The only reviewed repository with an implemented Python/Flask backend, `POST /api/command`, REST JSON communication, and explicit Flask dependencies. It is the strongest existing source of backend evidence and should be audited before any visibility decision. |
| `RTM-Real-Time-Multiplayer` | Private | **KEEP** | A distinct real-time collaboration experiment with a WebSocket server, VS Code extension, lint, and test scripts. It is not Python-focused, but demonstrates networking and tooling work without adding public-profile clutter. |
| `Horavia` | Public | **KEEP** | A comparatively complete application with Supabase, Stripe, Zod, Vitest, lint, typecheck, and a documented credential-free demo. Keep as transferable engineering evidence until stronger public Python projects exist. |
| `plataforma-de-pedidos-online-` | Public | **KEEP** | Mesaora documents a coherent end-to-end product flow and includes Playwright, lint, tests, and typecheck. It provides current evidence of testing and structured delivery even though its stack is frontend-focused. |
| `pratele` | Public | **ARCHIVE** | A polished and tested catalog demo with Vitest, Playwright, accessibility checks, CI, and a live demo. Preserve the evidence, but archive it after pinning or documenting the strongest transferable work because it no longer matches the target direction. |
| `ritmoar` | Public | **ARCHIVE** | Substantial React/TypeScript product demo with Playwright, lint, tests, and typecheck. Preserve it as completed historical work; it is not aligned with the new backend focus. |
| `trilhara` | Public | **ARCHIVE** | Functional learning-product demo with Playwright, lint, tests, typecheck, and a published demo. It is useful historical evidence but overlaps the frontend-heavy public portfolio. |
| `corporate-minimalist-dashboard` | Public | **ARCHIVE** | Navigable UI prototype derived from a Figma concept, with build scripts but no listed test or typecheck script. Preserve it read-only rather than presenting it as current work. |
| `Portifolio` | Public | **CONSIDER DELETION AFTER BACKUP** | The repository is explicitly frontend-positioned and conflicts with the new career direction. It also contains unique personal assets and structured content, so deletion must wait for a verified backup and link migration. |
| `Personal-Finance-Web-App` | Public | **CONSIDER DELETION AFTER BACKUP** | The default branch contains only a README and ignore files; the described application and technologies are planned rather than implemented. A separate development branch exists, so inspect and back it up before any decision. |
| `loja-virtual-de-moda` | Public | **CONSIDER DELETION AFTER BACKUP** | One of several overlapping ecommerce demos with the same build scripts and a near-identical dependency footprint. Preserve only if its domain-specific visual work is still useful. |
| `loja-virtual-profissional` | Public | **CONSIDER DELETION AFTER BACKUP** | Marketplace-style ecommerce demo that substantially overlaps the other storefront repositories in purpose and tooling. Back up screenshots and any unique components first. |
| `Premium-Custom-E-commerce-Layout` | Public | **CONSIDER DELETION AFTER BACKUP** | Visual ecommerce layout with overlapping React/Vite tooling and no listed lint, typecheck, or test scripts. Back up unique premium-layout assets before deletion. |
| `loja-virtual-de-materiais-de-construcao` | Public | **CONSIDER DELETION AFTER BACKUP** | Another ecommerce variation with the same build-script pattern and overlapping dependencies. Back up any unique catalog data and construction-specific visual assets first. |

## Required backup before any future Portifolio deletion

The following paths hold data that is not safely replaced by the new profile README:

- `public/documents/curriculo-hamilton-felipe.pdf` — current resume artifact;
- `public/images/felipe.jpeg` and the illustrated portrait assets — personal source
  media;
- `public/images/hamilton-felipe-curriculo.jpg` — resume preview;
- `src/data/projects.ts` — project records and verified links;
- `src/lib/site.ts` — public identity and site metadata;
- `src/lib/contact.ts` — contact-channel configuration;
- `src/lib/translations.ts` — bilingual professional copy;
- `.env.example` — variable names required to reconstruct integrations;
- `README.md` — deployment, technology, and project inventory;
- the latest deploy URL and its configuration, recorded separately from the source
  backup.

Before deletion, create a versioned archive, verify that it can be opened, record
the final commit hash, and update or remove every inbound link that still points to
the portfolio. Deleting the repository would not automatically remove a separately
hosted deployment.

## Suggested order

1. Keep the profile, Code Farming, Horavia, Mesaora, and RTM while public Python
   evidence is still limited.
2. Publish one maintainable Python API and one useful automation project.
3. Revisit pins and archive the completed frontend demos.
4. Back up and inspect every non-default branch before considering deletion.
5. Perform deletion only in a separate, explicitly authorized task.
