# Tasks

Live checklist. Update in the same commit as the work it tracks. Governed by `spec/index.md`; phases follow `plan.md`.

## Phase 0 — Scaffolding

- [x] `spec/index.md`
- [x] `plan.md`
- [x] `tasks.md`
- [ ] `.gitignore` (node_modules, build, .svelte-kit, .DS_Store)
- [ ] `spec/maturity-model.md` (Initiate / Develop / Standardize / Manage / Orchestrate, written for agile service management)
- [ ] `spec/topics.tsv` (part, number, slug, title) generated from spec §4
- [ ] `AGENTS.md` and `AGENTS/` role cards (researcher, topic-author, reviewer, reference-editor, site-developer)
- [ ] `CLAUDE.md` (a short pointer to `AGENTS.md` and the spec)
- [ ] `STYLE_GUIDE.md` (en-001 conventions, voice, prompt-writing style)
- [ ] `bin/` vendored from public-value-guide: `locale-peer-id`, `grep-locale-peer-id`, `slug-case`, `markdown-read-to-headline`
- [ ] `bin/check` adapted: slug-only directories, 15-section template, `README.md` symlink check, AI prompt and skill-link checks, `--links` Wikipedia check
- [ ] `bin/build-llms` adapted to read `spec/topics.tsv`
- [ ] `bin/deploy-site` (`git subtree push --prefix=agile-itil.github.io site main`)
- [ ] `locales/en-001/topics/.locale-peer-id`
- [ ] For all 50 topics: `locales/en-001/topics/<slug>/` with `index.md` stub, `README.md -> index.md` relative symlink, and `.locale-peer-id`
- [ ] `README.md` (table of contents, who the guide is for, how to use it, trademark notice; no preface), `GLOSSARY.md`, `INDEX.md` skeletons
- [ ] `CITATION.cff`
- [ ] `_sources/research-notes.md` skeleton
- [ ] Copy relevant skills from `~/git/skills-on-ai/skills-on-ai/skills` into `skills/` (whole directories, unchanged), and record them in `skills/README.md`. Starting list:
  - Agile: `agile-charter`, `agile-coaching`, `agile-delivery`, `agile-discovery`, `agile-liftoff`, `agile-principles`, `agile-reflection`, `agile-showcase`, `agile-standown`, `agile-standup`, `scrum`, `scrum-of-scrums`, `scrumban`, `kanban`, `extreme-programming`, `large-scale-scrum`, `scaled-agile-framework`, `disciplined-agile`, `user-story`, `feature-prioritization`, `product-roadmap`, `futurespective`, `team-focus`
  - Lean and improvement: `kaizen`, `value-stream-map`, `six-sigma`, `dmaic`
  - Service management: `service-catalog`, `service-level-agreement`, `change-request`, `release-notes`, `changelog`, `configuration-management`, `incident-response-plan`, `postmortem`, `runbook`, `on-call-rotation`, `capacity-planning`, `demand-analysis`, `demand-forecasting`, `business-continuity-plan`, `disaster-recovery-plan`, `disaster-recovery-testing`, `vendor-management`
  - Governance and risk: `risk-register`, `key-risk-indicators`, `risks-actions-issues-decisions`, `raci-matrix`, `enterprise-change-management`, `portfolio-management`
  - AI: `prompt-engineering`
- [ ] Rescan the skills source for further matches (asset, license, metrics, OKR, DevOps, SRE, facilitation) and add any that topics will link to

## Phase 1 — Research

- [ ] Read and take notes on the six core Wikipedia articles (spec §6 item 3)
- [ ] Verify primary sources per part (Agile Manifesto, Scrum Guide, Kanban Guide, ITIL 4 owner material, ISO/IEC scope statements, DORA, SRE books)
- [ ] Record verified Wikipedia slugs for every topic in `_sources/research-notes.md`
- [ ] Confirm or revise the spec §4 manifest and scope notes before any prose is written

## Phase 2 — Canonical topics (`en-001`)

### Part 1 — Agile foundations

- [ ] 1.1 Agile Manifesto — `agile-manifesto`
- [ ] 1.2 Agile Principles — `agile-principles`
- [ ] 1.3 Agile Software Development — `agile-software-development`
- [ ] 1.4 Scrum — `scrum`
- [ ] 1.5 Kanban — `kanban`
- [ ] 1.6 Extreme Programming — `extreme-programming`
- [ ] 1.7 Lean Software Development — `lean-software-development`
- [ ] 1.8 Scaling Agile — `scaling-agile`
- [ ] 1.9 Agile Management — `agile-management`
- [ ] 1.10 Agile Learning — `agile-learning`

### Part 2 — ITIL and IT service management foundations

- [ ] 2.1 IT Service Management — `it-service-management`
- [ ] 2.2 ITIL — `itil`
- [ ] 2.3 The ITIL Service Value System — `service-value-system`
- [ ] 2.4 ITIL Guiding Principles — `itil-guiding-principles`
- [ ] 2.5 Four Dimensions of Service Management — `four-dimensions-of-service-management`
- [ ] 2.6 The Service Value Chain — `service-value-chain`
- [ ] 2.7 ITSM Frameworks and Standards — `itsm-frameworks-and-standards`

### Part 3 — Service practices, the agile way

- [ ] 3.1 Service Desk — `service-desk`
- [ ] 3.2 Incident Management — `incident-management`
- [ ] 3.3 Problem Management — `problem-management`
- [ ] 3.4 Change Enablement — `change-enablement`
- [ ] 3.5 Release and Deployment Management — `release-and-deployment-management`
- [ ] 3.6 Service Request Management — `service-request-management`
- [ ] 3.7 Service Level Management — `service-level-management`
- [ ] 3.8 Service Catalog Management — `service-catalog-management`
- [ ] 3.9 Knowledge Management — `knowledge-management`
- [ ] 3.10 Monitoring and Event Management — `monitoring-and-event-management`
- [ ] 3.11 Availability, Capacity, and Performance — `availability-capacity-and-performance`
- [ ] 3.12 Service Continuity Management — `service-continuity-management`
- [ ] 3.13 Information Security Management — `information-security-management`
- [ ] 3.14 Supplier Management — `supplier-management`
- [ ] 3.15 Continual Improvement — `continual-improvement`

### Part 4 — IT asset and configuration management

- [ ] 4.1 IT Asset Management — `it-asset-management`
- [ ] 4.2 Software Asset Management — `software-asset-management`
- [ ] 4.3 Hardware Asset Management — `hardware-asset-management`
- [ ] 4.4 Configuration Management — `configuration-management`
- [ ] 4.5 IT Financial Management and FinOps — `it-financial-management-and-finops`

### Part 5 — Bringing agile and ITIL together

- [ ] 5.1 Agile Service Management — `agile-service-management`
- [ ] 5.2 DevOps — `devops`
- [ ] 5.3 Site Reliability Engineering — `site-reliability-engineering`
- [ ] 5.4 Value Stream Management — `value-stream-management`
- [ ] 5.5 Product and Service Ownership — `product-and-service-ownership`
- [ ] 5.6 Metrics and Measurement — `metrics-and-measurement`
- [ ] 5.7 Governance, Risk, and Compliance — `governance-risk-and-compliance`
- [ ] 5.8 Organizational Change and Adoption — `organizational-change-and-adoption`

### Part 6 — People, conversations, and AI

- [ ] 6.1 Team Conversations — `team-conversations`
- [ ] 6.2 AI in IT Service Management — `ai-in-it-service-management`
- [ ] 6.3 AI Skills and Prompts — `ai-skills-and-prompts`
- [ ] 6.4 Learning Paths and Certification — `learning-paths-and-certification`

## Phase 3 — Reference matter and skills

- [ ] `GLOSSARY.md` reconciled after each part (1–6)
- [ ] `INDEX.md` reconciled after each part (1–6)
- [ ] `skills/agile-itil-guide-skill/SKILL.md` (for readers)
- [ ] `skills/agile-itil-guide-maintainer-skill/SKILL.md` (for maintainers)
- [ ] Prune unlinked copied skills; every copied skill is linked from at least one topic (spec §7)
- [ ] `bin/build-llms` run; `llms.txt` and `llms.json` committed

## Phase 4 — Quality gates

- [ ] `bin/check` passes for all topics (structural and offline consistency)
- [ ] `bin/check --links` passes (Wikipedia links live, skill links resolve)
- [ ] Source gate review on every topic (no invented sources or figures; no long copyrighted excerpts)
- [ ] Consistency gate review (cross-references carry number and title; acronyms expanded)

## Phase 5 — Website subproject (`agile-itil.github.io/`)

- [ ] Scaffold SvelteKit 3 + Svelte 5 + adapter-static + TypeScript with pnpm (`package.json` with `packageManager`, `pnpm-lock.yaml`, `pnpm-workspace.yaml`, `vite.config.ts`, `tsconfig.json`)
- [ ] Install `@lilydesignsystem/svelte-headless`, `@lilydesignsystem/svelte-picker-bar`, `@lilydesignsystem/themes` (check current versions on npmjs.com)
- [ ] `scripts/sync-themes.sh` (postinstall; generic default themes only)
- [ ] Confirm and install the Sveltia i18n package; `src/lib/locales/en-001.json` UI strings
- [ ] `scripts/sync-content.sh` (copies locales, glossary, index, skills, topics.tsv, llms files from the monorepo)
- [ ] `src/lib/book.ts` (parts, locales) reading `spec/topics.tsv`; `src/lib/server/book.ts`; `src/lib/markdown.ts`
- [ ] Routes: `/` locale redirect and search, `/[locale]/contents/`, `/[locale]/topics/[slug]/`, `/glossary/`, `/index/`, `/skills/`, `/sitemap.xml`
- [ ] Layout with `GrailLayout` and `PickerBar` (locale, theme, text size, search, links)
- [ ] `scripts/build-search-index.mjs` and search UI
- [ ] `static/assets/style.css`, favicon, `robots.txt`, `.nojekyll`
- [ ] `.github/workflows/deploy.yml` (pnpm/action-setup, `pnpm install --frozen-lockfile`, `pnpm build`, deploy to Pages)
- [ ] Subproject `README.md`, `AGENTS.md`, `spec/` (ported Lily picker-bar and search specs)
- [ ] `pnpm check` 0 errors; `pnpm build` clean
- [ ] Browser check of `build/` served statically at 1440px and 390px

## Phase 6 — Release

- [ ] `README.md`, `GLOSSARY.md`, `INDEX.md`, `spec/topics.tsv`, `llms.*` agree with spec §4
- [ ] Create GitHub repositories and add the `site` remote (confirm names with the maintainer)
- [ ] First `bin/deploy-site` subtree push; Pages site live and checked
- [ ] All tasks above checked off
