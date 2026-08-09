# Sijil — سِجِلّ

**Sijil** means a record or register: something written so knowledge, decisions, and history remain traceable over time.

Sijil is a reusable bootstrap contract for creating a repository-local project wiki maintained by humans and AI agents.

The template establishes three distinct knowledge layers:

- **Sources** hold evidence and authoritative product/engineering contracts.
- **Notes** synthesize the current project state across those sources.
- **Tasks** turn accepted direction, risks, and gaps into observable work.

It also installs authority rules, decision and correction records, an append-only knowledge log, page templates, and mechanical wiki linting.

## Quick start — one action

In the project you want to initialize, give your AI coding agent this instruction:

```text
Initialize this project with https://github.com/Alkhayal7/sijil
```

That is the complete user workflow. The agent should open Sijil, discover the entry point below, inspect the user's current project, create and seed its wiki, integrate validation with its existing command interface, and report decisions that still require the project owner. The user does not need to clone Sijil or copy files manually.

## Agent entry point

If you are an AI agent given the Sijil repository URL to initialize another project:

1. Treat the repository open in your current workspace as the **target project**.
2. Read [`WIKI_BOOTSTRAP.md`](WIKI_BOOTSTRAP.md) completely before making changes.
3. Use Sijil as instructions only. Do not replace the target with this repository or copy Sijil's `README.md` or `AGENTS.md` into it.
4. Follow the bootstrap sections in order: inspect → map domains and authority → create and seed → integrate validation → verify → hand off.
5. Make changes only in the target project. Preserve its existing instructions and uncommitted work.

If you reached this README through a browser or repository tool, the direct contract is:

```text
https://raw.githubusercontent.com/Alkhayal7/sijil/main/WIKI_BOOTSTRAP.md
```

The bootstrap is intentionally an instruction document rather than a prefilled wiki. This prevents product decisions, architecture, task IDs, and terminology from one project leaking into another.

## Optional owner context

The agent can begin from repository evidence alone. Results improve if you also provide:

- the product concept or founding brief;
- intended users and explicit non-goals;
- accepted architecture constraints;
- the current delivery milestone;
- decision owners and regulated/geographic scope;
- the command that must pass before handoff.

Informal context does not become durable truth until the initializing agent records it in the appropriate source.

## Repository contents

| File | Purpose |
|---|---|
| [`WIKI_BOOTSTRAP.md`](WIKI_BOOTSTRAP.md) | Complete initialization and maintenance instructions for an AI agent |
| [`AGENTS.md`](AGENTS.md) | Rules for maintaining this reusable template repository |
