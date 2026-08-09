# Project Wiki Template

A reusable bootstrap contract for creating a repository-local project wiki maintained by humans and AI agents.

The template establishes three distinct knowledge layers:

- **Sources** hold evidence and authoritative product/engineering contracts.
- **Notes** synthesize the current project state across those sources.
- **Tasks** turn accepted direction, risks, and gaps into observable work.

It also installs authority rules, decision and correction records, an append-only knowledge log, page templates, and mechanical wiki linting.

## Use it in a new project

Clone this repository somewhere convenient:

```bash
git clone <this-repository-url> project-wiki-template
```

Open your target project with an AI coding agent and provide it with [`WIKI_BOOTSTRAP.md`](WIKI_BOOTSTRAP.md). Use this request:

```text
Follow WIKI_BOOTSTRAP.md in full to initialize and seed this project's wiki.
Inspect the target repository before editing it. Adapt the domains and authority
map to this project, preserve existing work, and run every required verification
before handoff.
```

The bootstrap is intentionally an instruction document rather than a prefilled wiki. This prevents product decisions, architecture, task IDs, and terminology from one project leaking into another.

## Use it in an existing project

Give the bootstrap document to the agent and tell it which repository is the target. The agent is required to inspect and preserve existing contributor instructions, documentation, task systems, command interfaces, and uncommitted work before integrating the wiki.

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

## License

No license has been selected yet. Add the license appropriate to how you intend to distribute the template before publishing it.
