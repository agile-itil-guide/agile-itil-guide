# Build plan

## What we are building

The *Agile ITIL Guide*: 6 parts, 49 topics (no preface), written in the canonical locale `en-001`. Every topic covers research, practices, a worked example, questions to discuss with your team, AI prompts, and links to AI skills. The monorepo also holds the AI skills (`skills/`), the tooling (`bin/`), and the reading website (`agile-itil.github.io/`), which is deployed by git subtree. Everything follows `spec/index.md`.

## Reference implementation

`~/git/public-value-guide` is the model for practices: spec-first authoring, `AGENTS.md` plus role cards, `STYLE_GUIDE.md`, `.locale-peer-id` files, `bin/check` quality gates, `bin/build-llms`, the reader and maintainer skills, and the SvelteKit + Lily Design System site. Copy and adapt its patterns. Do not copy its content. Differences on purpose:

- Directory slugs carry no number (`agile-manifesto/`, not `01-01-agile-manifesto/`). Ordering lives in `spec/index.md` §4 and `spec/topics.tsv`.
- Each topic directory has `README.md -> index.md` (relative symlink).
- No preface: the guide opens with Topic 1.1, and preface-style material lives in `README.md`.
- One locale (`en-001`) at launch, rather than many.
- The topic template adds `## AI prompts` and `## AI skills`, and replaces the sector lenses with four perspectives (product and delivery, service and operations, leadership and governance, customers and users).
- The website lives inside the monorepo as `agile-itil.github.io/`, uses pnpm (as the reference site does), uses Sveltia i18n for UI strings, and is deployed with `git subtree push`.

## Grounding sources

The six Wikipedia articles named in `spec/index.md` §6 item 3 are the starting point: Agile software development, Agile learning, Agile management, ITIL, IT service management, and IT asset management. From them, follow their cited primary sources: agilemanifesto.org, the Scrum Guide, the Kanban Guide, ITIL 4 material from the framework owner, ISO/IEC 20000/19770/27001 scope statements, DORA research, Google's SRE books, and the Lean/DevOps literature. `_sources/research-notes.md` collects verified findings per part as research proceeds. Every claim is checked against a live source before it is cited (spec §6).

## Phases

**Phase 0 — Scaffolding** (before any topic prose)
Monorepo layout; `AGENTS.md`, `AGENTS/` role cards, `CLAUDE.md`; `STYLE_GUIDE.md`; `spec/maturity-model.md` and `spec/topics.tsv`; `bin/` tools vendored from public-value-guide and adapted (slug-only directories, 15-section template, symlink and skill-link checks); `locales/en-001/topics/<slug>/` for all 49 topics, each with an empty `index.md` stub, `README.md -> index.md`, and `.locale-peer-id`; copied skills in `skills/` plus `skills/README.md`; skeletons for `README.md`, `GLOSSARY.md`, `INDEX.md`, `CITATION.cff`, `_sources/research-notes.md`, and `.gitignore`. Commit after each item.

**Phase 1 — Research**
Read the six core Wikipedia articles and their key primary sources; write `_sources/research-notes.md` by part, including verified Wikipedia slugs for each topic. Note topic boundaries where the sources overlap (for example ITIL change enablement versus DevOps continuous delivery) and confirm the scope notes in spec §4, changing the manifest now if needed: renumbering later costs much more.

**Phase 2 — Canonical topics, part by part**
Write the topics in order (there is no preface; spec §4), Part 1 to Part 6, one topic per commit. Later parts depend on earlier concepts (Part 5 assumes Parts 1–3), so do not skip ahead. Part 6 comes last because Topic 6.1 collects conversation starters and Topic 6.3 explains the prompt and skill conventions used throughout.

**Phase 3 — Reference matter and skills**
Each topic author adds their new terms to `GLOSSARY.md` and `INDEX.md` in the same commit; a reference-editor pass reconciles them at the end of each part. Write the two original skills (`agile-itil-guide-skill`, `agile-itil-guide-maintainer-skill`) once Part 2 is done, so they can reference real topics, and refine them at the end. Prune or add copied skills so that every copied skill is linked from at least one topic (spec §7).

**Phase 4 — Quality gates**
A reviewer runs the four gates (spec §11) on every topic, using `bin/check` and `bin/check --links`, and fixes findings, worst first.

**Phase 5 — Website subproject**
Scaffold `agile-itil.github.io/` from the public-value-guide site: SvelteKit 3, adapter-static, `@lilydesignsystem/svelte-headless`, `svelte-picker-bar`, and `themes`, Sveltia i18n, the build-time search index, sitemap, and `/skills/` pages; `scripts/sync-content.sh` pulling from the monorepo; the GitHub Actions Pages workflow; `bin/deploy-site` for `git subtree push`. The site can be built in parallel with Phase 2 once enough topics exist (Part 1) to exercise the templates; it ships only after Phase 4.

**Phase 6 — Release**
`README.md`, `GLOSSARY.md`, `INDEX.md`, `spec/topics.tsv`, and `llms.txt`/`llms.json` agree with spec §4; `bin/check --links` passes; the site builds and has been checked in a browser; first subtree deploy; `tasks.md` fully checked off.

## Working method

- Spec first: if a task needs a decision the spec does not cover, update the spec in the same commit.
- Commit automatically as work progresses: one logical change per commit, with the harness's `Co-Authored-By` trailer. Commits may be SSH-signed; if a commit hangs, ask the maintainer to run `ssh-add`.
- One writer per file; work serially unless the maintainer asks for parallel agents.
- After any interrupted batch, check what reached disk before re-running.
- Update `tasks.md` in the same commit as the work it tracks.

## Key decisions to confirm with the maintainer

1. **Manifest size.** 49 topics is ambitious. Parts 3 and 4 could be trimmed (for example by merging hardware and software asset management) if a smaller first release is preferred.
2. **GitHub organization and remotes.** The plan assumes `agile-itil/agile-itil-guide` for the monorepo and `agile-itil/agile-itil.github.io` for the site (remote name `site`). Both repositories need creating before the first push.
3. **Sveltia i18n package.** Confirm the exact npm registry package and version before Phase 5 (spec §9).

## Risks and mitigations

- **Copyrighted framework text** (ITIL, ISO standards): summarize and cite, never reproduce at length; the source gate checks this.
- **Framework partisanship** ("ITIL is bureaucracy" / "agile is chaos"): the style rules (spec §5) and the four-perspectives section force balance.
- **AI prompts that invite hallucination:** spec §3 item 12 forbids prompts that ask an AI to invent metrics, sources, or compliance claims; prompts use explicit placeholders and verification steps.
- **Scope overlap among 49 topics:** every contested concept has one home topic named in the spec §4 scope notes; others cross-reference it.
- **Subtree drift:** the site repository is never edited directly; `bin/deploy-site` is the only way to publish.
- **Stale copied skills:** `skills/README.md` records each skill's source; re-copy rather than edit locally.
