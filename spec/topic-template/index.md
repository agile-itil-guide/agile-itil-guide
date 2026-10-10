# Topic template

Governed by `spec/index.md`, which points here. Every topic has exactly these sections, in this order, with these exact headings:

1. `# Title`: the first headline of the topic's `index.md` is the topic title and the single source of truth for it. Nothing else (a manifest, a table of contents, a cross-reference) defines the title; those copy it from here. Topic numbers live in the table of contents, not in headings or directory names.
2. A bold one-sentence thesis (no heading above it).
3. `## Why this matters`
4. `## Core concepts`
5. `## Best practices`: numbered list, 8–12 items. Each item has a bold lead-in followed by 2–4 sentences.
6. `## Questions to discuss with your team`: **exactly six** questions. Each question is bold and followed by a 3–6 sentence briefing that helps a facilitator run the conversation.
7. `## In practice: an agile ITIL example`: one fictional worked scenario set in a named *type* of organization (for example "a mid-sized online retailer" or "a regional hospital's IT department"), never a real named company.
8. `## Four perspectives`: exactly these four subsections, in this order:
   - `### Product and delivery teams`
   - `### Service and operations teams`
   - `### Leadership and governance`
   - `### Customers and users`
9. `## Common failure modes`: 5–8 bulleted anti-patterns, each with what to do instead.
10. `## Maturity model`: a table with the five columns **Initiate / Develop / Standardize / Manage / Orchestrate** (see `spec/maturity-model.md`) and 3–5 rows.
11. `## Checklist`: 6–12 `- [ ]` items.
12. `## AI prompts`: 3–5 prompts. Each has a bold one-line purpose, then a fenced `text` block the reader can copy and paste. Each prompt asks the reader to fill in placeholders written in `[square brackets]`. No prompt may ask an AI to invent metrics, sources, or compliance claims.
13. `## AI skills`: 1–5 bullet links to relevant skills in `skills/`, written as relative links (`[scrum](../../../../skills/scrum/SKILL.md)`), each with one sentence on when to use it. Every linked skill must exist.
14. `## Key sources`: the 3–6 most useful works for further reading, each with one sentence on why it is useful.
15. `## References`: a numbered list combining Wikipedia articles and other authoritative sources, in the format `Title — Publisher/Author — URL`.

No section may be renamed, reordered, merged, or left out. The template is identical for every topic in every part, with no exceptions.
