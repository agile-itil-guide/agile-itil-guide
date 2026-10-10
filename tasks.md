# Tasks

Live checklist. Update in the same commit as the work it tracks. Governed by `spec/index.md`; phases follow `plan.md`.

## Phase 0 — Scaffolding

- [x] `spec/index.md`
- [x] `plan.md`
- [x] `tasks.md`
- [x] `.gitignore` (node_modules, build, .svelte-kit, .DS_Store)
- [x] `spec/maturity-model.md` (Initiate / Develop / Standardize / Manage / Orchestrate, written for agile service management)
- [x] `spec/topics.tsv` (part, number, slug, title) generated from spec §4
- [x] `AGENTS.md` and `AGENTS/` role cards (researcher, topic-author, reviewer, reference-editor, site-developer)
- [x] `CLAUDE.md` (a short pointer to `AGENTS.md` and the spec)
- [x] `STYLE_GUIDE.md` (en-001 conventions, voice, prompt-writing style)
- [x] `bin/` vendored from public-value-guide: `locale-peer-id`, `grep-locale-peer-id`, `slug-case`, `markdown-read-to-headline`
- [x] `bin/check` adapted: slug-only directories, 15-section template, `README.md` symlink check, AI prompt and skill-link checks, `--links` Wikipedia check
- [x] `bin/build-llms` adapted to read `spec/topics.tsv`; `bin/build-readme` added
- [x] `bin/deploy-site` (`git subtree push --prefix=agile-itil.github.io site main`)
- [x] `locales/en-001/topics/.locale-peer-id`
- [x] For all 49 topics: `locales/en-001/topics/<slug>/` with `index.md` stub, `README.md -> index.md` relative symlink, and `.locale-peer-id`
- [x] `README.md` (table of contents, who the guide is for, how to use it, trademark notice; no preface), `GLOSSARY.md`, `INDEX.md` skeletons
- [x] `CITATION.cff`
- [x] `_sources/research-notes.md` skeleton
- [x] Copy relevant skills (84 copied; see `skills/README.md`; pruned in Phase 3) from `~/git/skills-on-ai/skills-on-ai/skills` into `skills/` (whole directories, unchanged), and record them in `skills/README.md`. Starting list:
  - Agile: `agile-charter`, `agile-coaching`, `agile-delivery`, `agile-discovery`, `agile-liftoff`, `agile-principles`, `agile-reflection`, `agile-showcase`, `agile-standown`, `agile-standup`, `scrum`, `scrum-of-scrums`, `scrumban`, `kanban`, `extreme-programming`, `large-scale-scrum`, `scaled-agile-framework`, `disciplined-agile`, `user-story`, `feature-prioritization`, `product-roadmap`, `futurespective`, `team-focus`
  - Lean and improvement: `kaizen`, `value-stream-map`, `six-sigma`, `dmaic`
  - Service management: `service-catalog`, `service-level-agreement`, `change-request`, `release-notes`, `changelog`, `configuration-management`, `incident-response-plan`, `postmortem`, `runbook`, `on-call-rotation`, `capacity-planning`, `demand-analysis`, `demand-forecasting`, `business-continuity-plan`, `disaster-recovery-plan`, `disaster-recovery-testing`, `vendor-management`
  - Governance and risk: `risk-register`, `key-risk-indicators`, `risks-actions-issues-decisions`, `raci-matrix`, `enterprise-change-management`, `portfolio-management`
  - AI: `prompt-engineering`
- [x] Rescan the skills source for further matches (asset, license, metrics, OKR, DevOps, SRE, facilitation) and add any that topics will link to

## Phase 1 — Research

- [x] Read and take notes on the six core Wikipedia articles (spec §6 item 3)
- [x] Verify primary sources per part (Agile Manifesto, Scrum Guide, Kanban Guide, ITIL 4 owner material, ISO/IEC scope statements, DORA, SRE books)
- [x] Record verified Wikipedia slugs for every topic in `_sources/research-notes.md`
- [x] Confirm or revise the spec §4 manifest and scope notes before any prose is written

## Phase 2 — Canonical topics (`en-001`)

### Part 1 — Agile foundations

- [x] 1.1 Agile Manifesto — `agile-manifesto`
- [x] 1.2 Agile Principles — `agile-principles`
- [x] 1.3 Agile Software Development — `agile-software-development`
- [x] 1.4 Scrum — `scrum`
- [x] 1.5 Kanban — `kanban`
- [x] 1.6 Extreme Programming — `extreme-programming`
- [x] 1.7 Lean Software Development — `lean-software-development`
- [x] 1.8 Scaling Agile — `scaling-agile`
- [x] 1.9 Agile Management — `agile-management`
- [x] 1.10 Agile Learning — `agile-learning`

### Part 2 — ITIL and IT service management foundations

- [x] 2.1 IT Service Management — `it-service-management`
- [x] 2.2 ITIL — `itil`
- [x] 2.3 The ITIL Service Value System — `service-value-system`
- [x] 2.4 ITIL Guiding Principles — `itil-guiding-principles`
- [x] 2.5 Four Dimensions of Service Management — `four-dimensions-of-service-management`
- [x] 2.6 The Service Value Chain — `service-value-chain`
- [x] 2.7 ITSM Frameworks and Standards — `itsm-frameworks-and-standards`

### Part 3 — Service practices, the agile way

- [x] 3.1 Service Desk — `service-desk`
- [x] 3.2 Incident Management — `incident-management`
- [x] 3.3 Problem Management — `problem-management`
- [x] 3.4 Change Enablement — `change-enablement`
- [x] 3.5 Release and Deployment Management — `release-and-deployment-management`
- [x] 3.6 Service Request Management — `service-request-management`
- [x] 3.7 Service Level Management — `service-level-management`
- [x] 3.8 Service Catalog Management — `service-catalog-management`
- [x] 3.9 Knowledge Management — `knowledge-management`
- [x] 3.10 Monitoring and Event Management — `monitoring-and-event-management`
- [x] 3.11 Availability, Capacity, and Performance — `availability-capacity-and-performance`
- [x] 3.12 Service Continuity Management — `service-continuity-management`
- [x] 3.13 Information Security Management — `information-security-management`
- [x] 3.14 Supplier Management — `supplier-management`
- [x] 3.15 Continual Improvement — `continual-improvement`

### Part 4 — IT asset and configuration management

- [x] 4.1 IT Asset Management — `it-asset-management`
- [x] 4.2 Software Asset Management — `software-asset-management`
- [x] 4.3 Hardware Asset Management — `hardware-asset-management`
- [x] 4.4 Configuration Management — `configuration-management`
- [x] 4.5 IT Financial Management and FinOps — `it-financial-management-and-finops`

### Part 5 — Bringing agile and ITIL together

- [x] 5.1 Agile Service Management — `agile-service-management`
- [x] 5.2 DevOps — `devops`
- [x] 5.3 Site Reliability Engineering — `site-reliability-engineering`
- [x] 5.4 Value Stream Management — `value-stream-management`
- [x] 5.5 Product and Service Ownership — `product-and-service-ownership`
- [x] 5.6 Metrics and Measurement — `metrics-and-measurement`
- [x] 5.7 Governance, Risk, and Compliance — `governance-risk-and-compliance`
- [x] 5.8 Organizational Change and Adoption — `organizational-change-and-adoption`

### Part 6 — People, conversations, and AI

- [x] 6.1 Team Conversations — `team-conversations`
- [x] 6.2 AI in IT Service Management — `ai-in-it-service-management`
- [x] 6.3 AI Skills and Prompts — `ai-skills-and-prompts`
- [x] 6.4 Learning Paths and Certification — `learning-paths-and-certification`

## Phase 3 — Reference matter and skills

- [x] `GLOSSARY.md` reconciled after each part (1–6)
- [x] `INDEX.md` reconciled after each part (1–6)
- [x] `skills/agile-itil-guide-skill/SKILL.md` (for readers)
- [x] `skills/agile-itil-guide-maintainer-skill/SKILL.md` (for maintainers)
- [x] Prune unlinked copied skills; every copied skill is linked from at least one topic (spec §7)
- [x] `bin/build-llms` run; `llms.txt` and `llms.json` committed

## Phase 4 — Quality gates

- [x] `bin/check` passes for all topics (structural and offline consistency)
- [x] `bin/check --links` passes (Wikipedia links live, skill links resolve)
- [ ] Source gate review on every topic (no invented sources or figures; no long copyrighted excerpts) — sources were read per topic and recorded in `_sources/research-notes.md`; a second-reader review is still open
- [x] Consistency gate review (cross-references carry number and title; acronyms expanded)
- [x] Style pass: add the one-time "service catalogue" parenthetical at first use of "service catalog" in each topic (STYLE_GUIDE.md, Language)

## Phase 5 — Website subproject (`agile-itil.github.io/`)

- [x] Scaffold SvelteKit 3 + Svelte 5 + adapter-static + TypeScript with pnpm (`package.json` with `packageManager`, `pnpm-lock.yaml`, `pnpm-workspace.yaml`, `vite.config.ts`, `tsconfig.json`)
- [x] Install `@lilydesignsystem/svelte-headless`, `@lilydesignsystem/svelte-picker-bar`, `@lilydesignsystem/themes` (check current versions on npmjs.com)
- [x] `scripts/sync-themes.sh` (postinstall; generic default themes only)
- [x] Confirm and install the Sveltia i18n package; `src/lib/locales/en-001.json` UI strings
- [x] `scripts/sync-content.sh` (copies locales, glossary, index, skills, topics.tsv, llms files from the monorepo)
- [x] `src/lib/book.ts` (parts, locales) reading `spec/topics.tsv`; `src/lib/server/book.ts`; `src/lib/markdown.ts`
- [x] Routes: `/` locale redirect and search, `/[locale]/contents/`, `/[locale]/topics/[slug]/`, `/glossary/`, `/index/`, `/skills/`, `/sitemap.xml`
- [x] Layout with `GrailLayout` and `PickerBar` (locale, theme, text size, search, links)
- [x] `scripts/build-search-index.mjs` and search UI
- [x] `static/assets/style.css`, favicon, `robots.txt`, `.nojekyll`
- [x] `.github/workflows/deploy.yml` (pnpm/action-setup, `pnpm install --frozen-lockfile`, `pnpm build`, deploy to Pages)
- [x] Subproject `README.md`, `AGENTS.md`, `spec/` (ported Lily picker-bar and search specs)
- [x] `pnpm check` 0 errors; `pnpm build` clean
- [x] Browser check of `build/` served statically at 1440px and 390px (checked with Topic 1.1: no horizontal scroll, 8 picker buttons, search works, console clean)

## Phase 6 — Release

- [x] `README.md`, `GLOSSARY.md`, `INDEX.md`, `spec/topics.tsv`, `llms.*` agree with spec §4
- [ ] Create GitHub repositories and add the `site` remote (confirm names with the maintainer)
- [ ] First `bin/deploy-site` subtree push; Pages site live and checked
- [ ] All tasks above checked off

## Phase 7 — Welsh (cy-gb) translation

Translate serially, one topic per commit, following `locales/cy-gb/TERMINOLOGY.md`. `bin/check` reads headings from `locales/cy-gb/locale.json`.

- [x] Scaffold `locales/cy-gb/` (peer ids, symlinks, titled stubs, `locale.json`, `TERMINOLOGY.md`) and make `bin/check` locale-aware
- [x] cy-gb 1.1 agile-manifesto
- [x] cy-gb 1.2 agile-principles
- [x] cy-gb 1.3 agile-software-development
- [x] cy-gb 1.4 scrum
- [x] cy-gb 1.5 kanban
- [x] cy-gb 1.6 extreme-programming
- [x] cy-gb 1.7 lean-software-development
- [x] cy-gb 1.8 scaling-agile
- [x] cy-gb 1.9 agile-management
- [x] cy-gb 1.10 agile-learning
- [x] cy-gb 2.1 it-service-management
- [x] cy-gb 2.2 itil
- [x] cy-gb 2.3 service-value-system
- [x] cy-gb 2.4 itil-guiding-principles
- [ ] cy-gb 2.5 four-dimensions-of-service-management
- [ ] cy-gb 2.6 service-value-chain
- [ ] cy-gb 2.7 itsm-frameworks-and-standards
- [ ] cy-gb 3.1 service-desk
- [ ] cy-gb 3.2 incident-management
- [ ] cy-gb 3.3 problem-management
- [ ] cy-gb 3.4 change-enablement
- [ ] cy-gb 3.5 release-and-deployment-management
- [ ] cy-gb 3.6 service-request-management
- [ ] cy-gb 3.7 service-level-management
- [ ] cy-gb 3.8 service-catalog-management
- [ ] cy-gb 3.9 knowledge-management
- [ ] cy-gb 3.10 monitoring-and-event-management
- [ ] cy-gb 3.11 availability-capacity-and-performance
- [ ] cy-gb 3.12 service-continuity-management
- [ ] cy-gb 3.13 information-security-management
- [ ] cy-gb 3.14 supplier-management
- [ ] cy-gb 3.15 continual-improvement
- [ ] cy-gb 4.1 it-asset-management
- [ ] cy-gb 4.2 software-asset-management
- [ ] cy-gb 4.3 hardware-asset-management
- [ ] cy-gb 4.4 configuration-management
- [ ] cy-gb 4.5 it-financial-management-and-finops
- [ ] cy-gb 5.1 agile-service-management
- [ ] cy-gb 5.2 devops
- [ ] cy-gb 5.3 site-reliability-engineering
- [ ] cy-gb 5.4 value-stream-management
- [ ] cy-gb 5.5 product-and-service-ownership
- [ ] cy-gb 5.6 metrics-and-measurement
- [ ] cy-gb 5.7 governance-risk-and-compliance
- [ ] cy-gb 5.8 organizational-change-and-adoption
- [ ] cy-gb 6.1 team-conversations
- [ ] cy-gb 6.2 ai-in-it-service-management
- [ ] cy-gb 6.3 ai-skills-and-prompts
- [ ] cy-gb 6.4 learning-paths-and-certification
- [ ] cy-gb GLOSSARY, INDEX, README, llms and site integration (locales.ts, messages, sync-content, search index)
- [ ] Welsh-speaking reviewer reads every translated topic
