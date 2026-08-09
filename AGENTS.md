# Template repository contract

This repository contains reusable, project-agnostic instructions. It does not describe any particular product.

When changing `WIKI_BOOTSTRAP.md`:

- keep product names, vendors, architectures, languages, frameworks, and milestones generic;
- distinguish mandatory knowledge-system invariants from examples an initializing agent may adapt;
- preserve the source → synthesis → task separation and explicit authority model;
- require agents to inspect a target repository before changing it;
- avoid adding dependencies or automation that the target project may not use;
- keep the bootstrap usable across capable AI coding agents;
- update `README.md` when usage or repository contents change;
- run `git diff --check` before handoff.

Do not add generated example wikis to this repository unless they are isolated fixtures clearly labeled as non-authoritative examples.
