# Research notes

Verified research behind the topics (plan.md Phase 1). Rules (spec §6):

- Record only what you read in a source this session, with the source URL beside it.
- Mark anything unverified as "unverified: do not cite".
- Verify each Wikipedia slug exists before listing it.

## Core sources

| Source | Used for | Read? |
|---|---|---|
| <https://en.wikipedia.org/wiki/Agile_software_development> | Parts 1, 5 | read (Oct 2026; partial: first ~100,000 characters of Agile_software_development) |
| <https://en.wikipedia.org/wiki/Agile_learning> | Topic 1.10, Part 6 | read (Oct 2026; partial: first ~100,000 characters of Agile_software_development) |
| <https://en.wikipedia.org/wiki/Agile_management> | Topic 1.9, Part 5 | read (Oct 2026; partial: first ~100,000 characters of Agile_software_development) |
| <https://en.wikipedia.org/wiki/ITIL> | Parts 2, 3 | read (Oct 2026) |
| <https://en.wikipedia.org/wiki/IT_service_management> | Parts 2, 3 | read (Oct 2026) |
| <https://en.wikipedia.org/wiki/IT_asset_management> | Part 4 | not yet |

## Part 1 — Agile foundations

Read in October 2026 (each URL fetched and summarized this session):

- <https://agilemanifesto.org/> and `/principles.html`, `/history.html`: four values, twelve principles, Snowbird 11–13 February 2001, 17 signatories. The principles page showed no copyright notice; topics paraphrase it and quote only phrases.
- <https://scrumguides.org/scrum-guide.html>: November 2020 edition, Schwaber and Sutherland, CC BY-SA 4.0; roles, events, artifacts, commitments, timebox limits.
- <https://kanbanguides.org/english/>: Kanban Guide v2025.5 (1 May 2025); three practices, four flow metrics, Definition of Workflow, service level expectation. The guide's licence section names CC BY 4.0 while its conventions section names BY-SA 4.0; cite neither.
- <https://less.works/less/framework/introduction>: LeSS (Larman and Vodde); LeSS (about 2–8 teams) and LeSS Huge (8 or more).
- Wikipedia (all fetched, summaries only): Agile_software_development, Agile_management, Agile_learning, Extreme_programming, Extreme_programming_practices, Kanban_(development), Lean_software_development, Lean_manufacturing, Scaled_agile_framework, Disciplined_agile_delivery.
- Not found: Wikipedia has no article at `Large-scale_Scrum` or `Large-Scale_Scrum` (HTTP 404); the topic cites less.works instead.
- Agile_learning: maintenance tags; evidence mostly German-language sources and conference papers. Agile_management: does not describe criticisms; says "agile project management" is not an international-standards term. Kanban_(development): conflict-of-interest tag.
- Verified Wikipedia slugs (via `bin/check --links`, 43 distinct as of Topic 1.10) are listed in each topic's References.
- Unverified, not cited: ThoughtWorks distributed XP claim (marked "citation needed" in the article, cited only as a claim); PMBOK Guide year (article says 2022).

## Part 2 — ITIL and IT service management foundations

Read in October 2026:

- Wikipedia (fetched, summaries only): IT_service_management (no history, criticism, or agile content; lists frameworks), ITIL (versions, owners, ITIL 4 and an ITIL 5 section dated January 2026; no criticisms), ISO/IEC_20000 (parts, 2018 edition, 2024 ISO survey figure), COBIT (flagged for weak sourcing), FitSM.
- <https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1> (owner): "The new ITIL is here!"; "Practical and AI-native by design"; ITIL Foundation / Product / Service / AI Governance (Version 5); ITIL 4 courses still listed; no release date; does not say whether ITIL 4 certificates are retired.
- <https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1/itil-4-foundation-2565> (owner): lists the four dimensions by name; names the service value system, guiding principles, service value chain without naming their contents.
- axelos.com pages fetched returned only a title (no usable body); not cited.
- Secondary (training provider and vendor), used only for descriptions and labelled as secondary in the topics: purplegriffon.com ITIL service value system page (six value chain activities and value stream definition); manageengine.com SVS page (lists activities, no descriptions); itsm.tools four dimensions page and search-result summaries (dimension descriptions, PESTLE).
- Wikipedia lists the seven guiding principles and the 34-practice count (22 + 12) under its ITIL 5 section; they match the widely published ITIL 4 structure, and the topics treat them as ITIL 4 concepts with a caution.
- Not verified, not cited: exact owner wording of the SVS components, the guiding principles, and the six activities (owner publications not read).

## Part 3 — Service practices, the agile way

Read in October 2026:

- Google *Site Reliability Engineering* book (sre.google/sre-book): Managing Incidents (Stribblehill), Postmortem Culture, Monitoring Distributed Systems, Practical Alerting from Time-Series Data, Service Level Objectives, Embracing Risk, Release Engineering. Treated as one organization's documented practice, not a universal rule.
- DORA (dora.dev): Streamlining change approval; Continuous delivery; software delivery performance metrics (five measures, including failed deployment recovery time and deployment rework rate). The pages cite the 2019 State of DevOps Report and give no effect sizes or sample details.
- Wikipedia (fetched, summaries only): Help_desk (short; no tiers, metrics, or history), Incident_management (multi-field), Root_cause_analysis, Service-level_agreement, Service_catalog, Knowledge_management (first 100,000 of 140,930 characters), Business_continuity_planning, Information_security (first 100,000 of 243,033 characters), ISO/IEC_27001, Supplier_relationship_management, Service_integration_and_management, Continual_improvement_process, PDCA, Capacity_planning.
- Not found or unusable: Wikipedia has no article at `Problem_management` or `Knowledge-centered_service` (HTTP 404); `Disaster_recovery` is only a disambiguation page; `Service_portfolio_management` redirects to IT_portfolio_management (no definition).
- ITIL vocabulary used in Part 3 (change types, known error, workaround, request model, event, underpinning contract, operational-level agreement, major incident) comes from widely published descriptions, not read from the framework owner; each topic says so. Verify against ITIL 4 publications before using exact definitions.
- axelos.com and peoplecert.org owner pages for practices were not available beyond the certification catalog.

## Part 4 — IT asset and configuration management

_No notes yet._

## Part 5 — Bringing agile and ITIL together

_No notes yet._

## Part 6 — People, conversations, and AI

_No notes yet._
