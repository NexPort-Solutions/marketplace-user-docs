# AGENTS: NexPort Marketplace Docs

Scope
- This file governs the entire repository. Follow these instructions for any file you add or modify.

Purpose
- This repo contains end‑user and admin documentation for NexPort Marketplace.
- Documentation is authored in Markdown and organized for GitBook.

Location (Important)
- All GitBook content lives under `user-docs/`.
- The GitBook entry files are `user-docs/README.md` and `user-docs/SUMMARY.md`.
- Images and other assets should be stored under `user-docs/assets/`.

Authoring Rules (GitBook‑Friendly)
- Markdown only. Avoid raw HTML and complex embeds.
- Use relative links between pages (e.g., `../admin/products.md`).
- Keep headings concise; prefer one H1 per page, then H2/H3 sparingly.
- Bullets should be short, one line where possible.
- Use blockquotes for callouts: `> Note`, `> Tip`, `> Warning`.
- Keep pages focused; split very long topics when a natural break exists.
- No secrets, tokens, or internal bug‑tracker links in public docs.

Project Structure
- `user-docs/` — GitBook docs root
  - `README.md` — Overview/landing page
  - `SUMMARY.md` — GitBook table of contents (required)
  - `user/` — End‑user guides
  - `admin/` — Admin guides
  - `reference/` — Glossary and reference
  - `assets/` — Images and static assets (create as needed)
- Repo root — Reference source materials only (e.g., whitepaper PDF, workflow docs, test suite). Do not reference internal links/IDs in published docs.

Style & Terminology
- Product names: NexPort Marketplace, NexPort Campus, NopCommerce.
- Use Title Case for section headers; sentence case for body text.
- Prefer active voice and present tense.
- Keep link text meaningful (avoid “click here”).
- When listing UI, match observed labels (e.g., `Administrator`, `Create/Edit Mapping`, `Redeem`).

Navigation Updates
- Any new page must be added to `user-docs/SUMMARY.md` to appear in GitBook navigation.
- Use lower‑case filenames with hyphens: `my-new-page.md`.

Content Sources (internal)
- Whitepaper (`Nexport Market Whitepaper.pdf`)
- Workflow notes (`SH Workflows in Marketplace.docx`, `SHCOE Workflows in Marketplace.docx`)
- Test suite (`nexport_campus_tests.xlsx`)
- When importing details, rewrite for customer‑facing clarity; exclude internal case IDs/links.

Operational Notes
- Do not document or recommend manually setting NopCommerce order status to Complete for mapped products (breaks redemption).
- Call out store‑level differences when features vary by brand/environment.
- Use examples with placeholder or example domains; avoid exposing real customer data.

Contribution Workflow
- One topic per PR; keep diffs small and focused.
- Validate Markdown renders correctly in GitBook (headings, lists, links, images).
- If adding images, compress and keep widths reasonable (≤1200px preferred) and store under `user-docs/assets/`.
- Update `user-docs/SUMMARY.md` alongside any new page.

Known Page Map (baseline under `user-docs/`)
- Overview: `README.md`
- End User: `user/` (getting started, registration, purchasing, redeeming, scholarships, FAQ)
- Admin: `admin/` (overview, stores, products, mapping, fixed vs open‑ended, scholarships/seats, wholesale, supplemental info, registration fields, orders, extensions/payments, reporting)
- Reference: `reference/glossary.md`

Contact
- If requirements change (new flows, labels), update both the relevant page(s) and this AGENTS file when guidance needs to change.

