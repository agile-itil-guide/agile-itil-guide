# CLAUDE.md

This repository is the *Agile ITIL Guide* (49 topics in 6 parts, locale `en-001`, plus AI skills and the `agile-itil.github.io/` website subproject). All operating instructions live in [`AGENTS.md`](AGENTS.md); the governing specification is [`spec/index.md`](spec/index.md), which wins wherever any file disagrees with it.

Read in this order: `spec/index.md` → `AGENTS.md` → the role card in `AGENTS/` for your task.

- Work serially. Do not use subagents, workflows, or fan-outs unless the maintainer asks.
- Commit automatically as work progresses, one logical change per commit, ending with the `Co-Authored-By` trailer the harness specifies.
- Use pnpm, never npm or yarn, in `agile-itil.github.io/`.
- After changing any topic, title, or skill, run `bin/build-llms` and `bin/check`.
