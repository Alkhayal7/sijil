# Sijil — سِجِلّ

**Sijil** means a record or register: something written so knowledge, decisions, and history remain traceable over time.

Sijil is a reusable bootstrap contract for creating a repository-local project wiki maintained by humans and AI agents.

The template establishes three distinct knowledge layers:

- **Sources** hold evidence and authoritative product/engineering contracts.
- **Notes** synthesize the current project state across those sources.
- **Tasks** turn accepted direction, risks, and gaps into observable work.

It also installs authority rules, decision and correction records, an append-only knowledge log, page templates, and mechanical wiki linting.

## Quick start — one action

Open the project you want to initialize in Codex or another capable coding agent, then send this prompt:

```text
Initialize this project with Sijil. Read and follow the bootstrap contract at
https://raw.githubusercontent.com/Alkhayal7/sijil/main/WIKI_BOOTSTRAP.md

Inspect this repository before editing it, adapt the wiki to its actual domains,
preserve existing work, and complete every required verification before handoff.
```

The agent should retrieve the contract, inspect the current repository, create and seed its wiki, integrate validation with its existing command interface, and report any decisions that still require the project owner. The user does not need to clone Sijil or copy files manually.

The bootstrap is intentionally an instruction document rather than a prefilled wiki. This prevents product decisions, architecture, task IDs, and terminology from one project leaking into another.

## Offline or restricted-agent fallback

If the agent cannot access GitHub, clone Sijil locally:

```bash
git clone https://github.com/Alkhayal7/sijil.git
```

Then attach or provide `sijil/WIKI_BOOTSTRAP.md` to the agent with this prompt:

```text
Follow WIKI_BOOTSTRAP.md in full to initialize and seed this project's wiki.
Inspect the target repository before editing it. Adapt the domains and authority
map to this project, preserve existing work, and run every required verification
before handoff.
```

The same workflow applies to new and existing projects. The contract requires the agent to preserve existing contributor instructions, documentation, task systems, command interfaces, and uncommitted work.

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
