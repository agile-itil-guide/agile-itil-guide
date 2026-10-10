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

- [ ] Read and take notes on the six core Wikipedia articles (spec §6 item 3)
- [ ] Verify primary sources per part (Agile Manifesto, Scrum Guide, Kanban Guide, ITIL 4 owner material, ISO/IEC scope statements, DORA, SRE books)
- [ ] Record verified Wikipedia slugs for every topic in `_sources/research-notes.md`
- [ ] Confirm or revise the spec §4 manifest and scope notes before any prose is written

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
- [x] `bin/build-llms` run; `llms.txt` and `llms.json` committed

## Phase 4 — Quality gates

- [x] `bin/check` passes for all topics (structural and offline consistency)
- [ ] `bin/check --links` passes (Wikipedia links live, skill links resolve)
- [ ] Source gate review on every topic (no invented sources or figures; no long copyrighted excerpts)
- [ ] Consistency gate review (cross-references carry number and title; acronyms expanded)

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

- [ ] `README.md`, `GLOSSARY.md`, `INDEX.md`, `spec/topics.tsv`, `llms.*` agree with spec §4
- [ ] Create GitHub repositories and add the `site` remote (confirm names with the maintainer)
- [ ] First `bin/deploy-site` subtree push; Pages site live and checked
- [ ] All tasks above checked off
