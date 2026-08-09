# Project Wiki Bootstrap Contract

You are responsible for creating and seeding a durable, repository-local wiki for the target project and for installing the operating contract that future human and AI contributors will follow.

Follow this document in full. Do not merely create empty folders. First understand the target repository, then build a useful wiki from evidence that actually exists. Adapt names and domains to the project. Never copy another project's product decisions, architecture, vendors, milestones, task IDs, or terminology.

## Invocation and navigation

When a user says `Initialize this project with https://github.com/Alkhayal7/sijil`, the repository already open in the agent's workspace is the **target project**. This Sijil repository is reference material, not the target.

Before acting:

1. Read this entire contract.
2. Return to the target project's root.
3. Follow the numbered sections in order.
4. Read and preserve the target's own agent/contributor instructions before editing.
5. Create wiki and integration files only inside the target project.
6. Do not copy Sijil's `README.md`, repository-level `AGENTS.md`, Git history, or branding into the target.

If the agent cannot determine which workspace/repository is the target, ask the user for its path before making changes.

## 1. Objective

Create a `wiki/` directory that becomes the project's persistent memory and provides:

- a clear hierarchy of authority;
- traceable product and engineering sources;
- concise current synthesis organized by real project domains;
- explicit decisions, contradictions, risks, assumptions, and unknowns;
- executable tasks with observable acceptance conditions;
- an append-only history of knowledge changes;
- navigation from one index;
- mechanical validation of structure, metadata, and links;
- repository-level instructions requiring the wiki to change alongside code.

The completed system must let a new contributor answer without relying on chat:

1. What is this project, who is it for, and what is out of scope?
2. What is true now, and which document owns each kind of claim?
3. How is the system divided, and which boundaries must not be crossed?
4. What was decided, by whom, why, and under what revisit condition?
5. What evidence supports time-sensitive claims, and when was it checked?
6. What work is ready, blocked, active, or verified complete?
7. Which command verifies the repository and wiki before handoff?

## 2. Non-negotiable principles

1. **The repository is project memory.** Chat, temporary plans, and agent context are not durable truth.
2. **Sources and synthesis are separate.** Sources own claims; maintained notes explain the current picture across sources.
3. **Authority is explicit.** Every material contract has one normative owner. Dependent documents link to that owner.
4. **Contradictions remain visible.** Never silently merge conflicting claims or choose a material product, legal, safety, cost, privacy, or architecture tradeoff without authorization.
5. **Tasks do not redefine specifications.** A checkbox, implementation, or test cannot silently override its owning contract.
6. **Completion is observable.** Mark work done only after its stated acceptance condition passes.
7. **External claims are dated.** Market, legal, pricing, security, vendor, and fast-changing technical claims require direct citations, geographic scope where relevant, and an evidence-check date.
8. **Truth changes propagate.** Update the owner, affected synthesis, decision/risk state, tasks, index, and append-only log together.
9. **Commands are stable.** Integrate wiki validation into the target repository's existing command interface.
10. **Initialization is evidence-led.** Label unsupported content as proposed, unknown, or needing an owner.

## 3. Inspect before editing

Read the target repository broadly enough to understand its current shape. At minimum inspect:

- every applicable `AGENTS.md` or equivalent contributor instruction;
- the root README and documentation entry points;
- manifests, lockfiles, build/task files, CI, tests, and source layout;
- product briefs, specifications, ADRs, plans, issue exports, research, and design sources;
- source-code dependency and ownership boundaries;
- Git status so existing user changes remain untouched;
- ignore rules and operational agent/tool configuration that belongs outside product documentation.

Use fast file and text search before opening files individually. Do not edit generated files, lockfiles, immutable imports, or unrelated user changes merely to make the wiki tidy.

Build an internal inventory of:

- project name and one-sentence thesis;
- intended users, scope, and explicit non-goals;
- lifecycle stage and observable delivery state;
- major product and engineering domains;
- authoritative documents already present;
- architecture and organizational boundaries;
- development commands and verification gates;
- unresolved contradictions and missing owners;
- material unknowns that cannot safely be inferred.

Ask the project owner only when a missing answer would materially change the wiki structure, authority model, or project direction. Otherwise proceed with a documented assumption and expose uncertainty.

## 4. Design the knowledge and authority maps

Choose domain hubs matching the project. Do not generate generic empty hubs. A small project may need three domains; a large project may need more.

For each domain, determine:

- scope and exclusions;
- normative product or engineering owner;
- maintained synthesis page;
- dependencies;
- accepted decisions and invariants;
- open risks, questions, and executable work.

Publish a conflict order. Use this baseline unless established project governance requires a different one:

1. the project owner's latest explicit decision;
2. an accepted correction/reconciliation record naming a normative owner;
3. accepted architecture decision records for architecture matters;
4. the domain-owning product or engineering specification;
5. dated primary research or official documentation;
6. maintained synthesis, plans, and task pages;
7. chat and unrecorded assumptions, which have no durable authority.

Preserve an existing formal hierarchy and document how it maps to the wiki.

## 5. Create the vault structure

Use this baseline, omitting optional branches that genuinely do not apply and documenting deliberate additions:

```text
wiki/
├── index.md
├── log.md
├── AGENTS.md
├── sources/
│   ├── product/
│   ├── specifications/
│   │   ├── README.md
│   │   └── CORRECTIONS.md
│   ├── research/
│   ├── design/                 # optional canonical design sources
│   └── external/
├── notes/
│   ├── overview/
│   ├── domains/
│   ├── decisions/
│   └── plans/
├── tasks/
├── assets/
│   └── inbox/
├── templates/
├── _meta/
│   ├── Schema.md
│   ├── Conventions.md
│   ├── Workflows.md
│   ├── Source Map.md
│   └── lint_vault.py
└── .obsidian/                  # optional plugin-free portable defaults
```

Layer contracts:

- `sources/product/`: evolving founding intent and product truth.
- `sources/specifications/`: evolving normative contracts and ownership/reconciliation maps.
- `sources/research/`: dated evidence dossiers with estimates and vendor claims labeled.
- `sources/design/`: canonical editable/executable design sources, not only screenshots.
- `sources/external/`: imported originals with provenance; treat them as immutable and supersede with new dated sources.
- `notes/`: maintained current synthesis linking to its sources and never inventing certainty.
- `tasks/`: executable state derived from sources, decisions, risks, and accepted plans.
- `_meta/`: schema, conventions, workflows, source map, and validation tooling.
- `templates/`: scaffolds, never project truth.
- `assets/`: media with provenance; unclassified additions enter `assets/inbox/`.

Do not relocate established authoritative files merely for symmetry if this breaks paths or ownership. The Source Map can reference files outside `wiki/`.

## 6. Install agent maintenance contracts

Create `wiki/AGENTS.md`. It must require future agents to:

1. read `wiki/index.md`;
2. read the relevant overview/domain hub;
3. read the owning sources linked by that hub;
4. check `sources/specifications/CORRECTIONS.md` before relying on cross-document contracts;
5. make the requested project change;
6. update affected sources, synthesis, decisions/risks, tasks, index, and log;
7. run a narrow check while iterating and the repository-wide gate before handoff.

It must define the layer model, authority order, link/metadata/evidence rules, contradiction handling, core workflows, append-only log format, and definition of done.

Add or carefully update the root `AGENTS.md` or equivalent. Preserve stricter existing instructions. It must:

- direct contributors to the wiki contract, index, relevant hub, owner, and corrections register before changing behavior;
- name the stable command interface and required handoff check;
- preserve actual architectural/module boundaries;
- prohibit production data, credentials, and paid/real integrations from default tests;
- require project-truth changes to update the full wiki chain;
- distinguish operational agent configuration from product authority.

## 7. Define schema and conventions

Document the directory model in `_meta/Schema.md`. Require YAML frontmatter on maintained notes, tasks, meta pages, and templates:

```yaml
---
title: Human-readable title
type: overview | domain | decision | plan | task-board | task-list | meta
status: current | draft | proposed | superseded | archived
updated: YYYY-MM-DD
owners:
  - role-or-person
sources:
  - "source-link"
tags:
  - project/domain
---
```

`owners` and `sources` may be absent only when genuinely inapplicable. `updated` means the last material content change. Do not bulk-add metadata to legacy sources when it obscures provenance.

Use existing stable IDs where available. Otherwise define project-appropriate schemes such as:

- existing ADR numbers for architecture decisions;
- `VD-NNN` for wiki decisions without a source ID;
- `C-NNN` for corrections;
- `T-NNN` for executable tasks;
- existing milestone/release identifiers rather than duplicates.

In `_meta/Conventions.md`, define readable subject filenames, full vault-root Wikilinks, direct external citations, ISO dates, page ownership, source sections, and explicit conflict callouts.

Knowledge statuses:

- `current`: best present synthesis;
- `draft`: incomplete and unsafe without source review;
- `proposed`: awaiting authorized decision;
- `superseded`: retained and linked to replacement;
- `archived`: inactive without direct replacement.

Task statuses:

- `backlog`: valid but not sequenced;
- `ready`: defined and unblocked;
- `in-progress`: actively owned;
- `blocked`: waiting on a named dependency;
- `done`: acceptance verified;
- `cancelled`: deliberately abandoned with reason.

A task must state outcome, owner role, source/decision, dependencies, and observable acceptance. “Needs research” is a task, not a blocker.

## 8. Seed evidence-backed content

Populate, based on repository evidence:

- `index.md`: thesis, delivery state, orientation, domains, authoritative sources, research, assets/design if relevant, and vault operations;
- an overview summarizing scope, boundaries, architecture, state, and major gates;
- one useful hub per real domain;
- `sources/specifications/README.md`: reading order and contract-to-owner map;
- `sources/specifications/CORRECTIONS.md`: owner map, conflicts, reconciliation history, invariants, unresolved decisions, and status date;
- `_meta/Source Map.md`: knowledge area → primary source → synthesis, including sources outside the vault;
- a Decision Register with stable ID, status, rationale, owner, evidence, consequences, alternatives, and revisit trigger;
- Open Questions and Risks with an owner or follow-up task for each material item;
- a canonical Task Board plus `Now`/`Backlog` views when scale warrants them;
- `log.md` with an initialization entry and no fabricated history.

Do not fill pages with generic prose. Record missing evidence or decisions as explicit questions/tasks. Every non-template page must be reachable from the index directly or through exactly one obvious hub.

## 9. Create templates

Create templates for domain synthesis, research/source notes, decisions, and tasks. Use the target project's name/tag namespace.

Templates must prompt for provenance, uncertainty, dependencies, and acceptance. The research template must request:

- research question;
- author/publisher;
- publication and retrieval dates;
- original URL or immutable local import;
- evidence type;
- cited findings;
- limits and uncertainty;
- implications for specifications, decisions, risks, or tasks;
- verification gaps and integration checklist.

## 10. Document workflows

In `_meta/Workflows.md`, define:

### Ingest a source

Classify and preserve provenance; read index/hubs/owners; extract decisions, constraints, disputed claims, risks, measurements, and unknowns; update affected synthesis; create follow-up tasks; update index/source map; append log; lint. Filing alone is not ingestion.

### Answer a project question

Start at the index and hub; read owning sources; apply authority rules; expose disagreement; cite sources; file reusable comparisons, plans, decisions, or risks.

### Change a specification

Identify the normative owner; update it first; reconcile duplicates or replace with owner links; update synthesis/plans/decisions/tasks; log and verify.

### Record a decision

Reuse an existing source/ADR/correction ID or allocate the next wiki ID; record status, owner, rationale, alternatives, dependencies, and revisit trigger; apply accepted decisions to the owning contract; update downstream knowledge/work.

### Maintain tasks

Add work to the canonical board/backlog; promote only defined unblocked tasks; change status when reality changes; mark done only after acceptance passes; fold results back into sources and synthesis.

## 11. Add mechanical validation

Create a small dependency-free `wiki/_meta/lint_vault.py`, or use the target project's native language when clearly preferable. Return nonzero on structural errors. Validate at least:

- required frontmatter;
- resolvable Wikilinks and local Markdown links;
- an index catalog entry for every non-excluded Markdown page;
- obvious orphan pages;
- research pages lacking a visible evidence date.

Distinguish errors from warnings and ignore links inside fenced/inline code.

Expose lint through the established command interface. For a Make-based repository:

```make
docs-lint: ## Validate the project wiki and local Markdown links.
	@python3 wiki/_meta/lint_vault.py
```

Include it in the repository-wide `check` target and CI. If the project uses another runner, extend it instead of introducing an overlapping tool/runtime. Do not add dependencies when the standard library is sufficient.

## 12. Log and verify initialization

Use append-only headings in `wiki/log.md`:

```text
## [YYYY-MM-DD] operation | concise title
```

Operations may include `initialize`, `ingest`, `change`, `decision`, `research`, `query`, `verification`, `lint`, and `structure`. Do not rewrite history except for a traceable correction of a malformed link or factual transcription error.

Before handoff:

1. inspect the diff and preserve unrelated work;
2. run wiki lint directly;
3. run the narrow documentation/check target;
4. run the repository-wide check;
5. fix errors instead of weakening checks;
6. report warnings and intentional exceptions;
7. confirm all pages are indexed/cross-linked;
8. confirm no secrets, production data, paid calls, or real integrations were used;
9. list assumptions and decisions requiring owner approval.

## 13. Definition of done

Initialization is complete only when:

- the repository and existing instructions were inspected first;
- the structure reflects actual project domains;
- authority and conflict rules are explicit;
- authoritative material is mapped without losing provenance;
- the index reliably routes to all knowledge;
- overview/domain hubs contain evidence-backed synthesis;
- contradictions, unknowns, and proposals are visible;
- decisions/tasks have stable IDs and owners;
- tasks have observable acceptance conditions;
- root/wiki agent contracts require continued maintenance;
- lint is part of the stable repository check path;
- initialization is appended to the log;
- wiki lint and repository-wide checks pass.

## 14. Required handoff

Lead with the outcome, then report:

- files created or updated;
- the project-specific authority/domain model;
- commands run and results;
- warnings and known gaps;
- decisions still owned by the project owner.

Use clickable repository links when supported. Never claim completion while an acceptance condition remains unverified.
