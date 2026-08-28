# Kiloloop

**Run a fleet of AI coding agents — portable, auditable, human-in-command.**

Kiloloop builds vendor-neutral tools for one loop: **plan** delegated AI work, **coordinate** it, and **learn** from every run. Coordination lives in plain files (no server), messages are signed and verifiable, and agents declare their scope up front — when a run drifts from its declaration, the protocol pauses it for a human. Everything here is maintained daily by the agent fleet it coordinates — the same protocol these repos document is the one that ships them.

## Products

- **[OACP](https://github.com/kiloloop/oacp)** — the Open Agent Coordination Protocol. Typed async messaging between agents (task dispatch, code review, handoff, brainstorm) plus persistent shared memory across agents, projects, and machines. File-based and runtime-agnostic: Claude Code, Codex, Gemini, or anything that reads YAML. Agents declare minutes, files, and side effects before work starts; mid-run checkpoints pause for human re-authorization when reality drifts from the declaration. v0.4 adds Ed25519-signed messages, an audit record for every autonomy decision, and a central store where every agent's session debrief lands as one immutable file. `pip install oacp-cli`

- **[agent-estimate](https://github.com/kiloloop/agent-estimate)** — know what an AI task will cost before you run it, and how the forecast held up after. PERT estimates calibrated for AI agents, human-equivalent compression ratios, METR reliability thresholds, and multi-agent wave planning. CLI, GitHub Action, and Claude Code plugin.

## Tools and skills

Drop-in pieces for your agent runtime, dogfooded daily by the fleet that maintains these repos:

- **[oacp-skills](https://github.com/kiloloop/oacp-skills)** — reusable skills for OACP agents: inbox processing, doctor, the author/reviewer review loop, org-memory synthesis, and session hygiene (self-improve, wrap-up).
- **[memory-lint](https://github.com/kiloloop/memory-lint)** — deterministic linter for AI agent memory files: broken wiki-links, index drift, stale entries, malformed frontmatter. Run it by hand or drop it in CI. `pip install memory-lint`
- **[kiloloop-skills](https://github.com/kiloloop/kiloloop-skills)** — agent-discipline skills for coding-agent runtimes (Claude Code, Codex): self-contained, versioned, fixture-tested. Shipping now:
  - `memory-lint` — lint memory corpora without modifying them
  - `proof-before-done` — execute completion claims, paste the evidence
  - `render-check` — review the surface a reader actually sees
  - `usage-cost` — local token usage priced at list rates
  - `verify-numbers` — check counts, deltas, and estimates before quoting them

## Research

Published from the fleet's internal pipeline, reviewed and sanitized before it lands in [kiloloop/research](https://github.com/kiloloop/research):

- **[Runtime capability matrix](https://github.com/kiloloop/research/blob/main/runtime-comparison/runtime_capability_matrix.md)** — Claude Code, Codex, and ZCode compared as coordination runtimes. Content CC BY 4.0.

## Examples & templates

Working examples you can fork, built on the products above:

- **[iantha](https://github.com/kiloloop/iantha)** — a personal chief of staff. Morning briefings, evening reviews, decision logs, optional Obsidian vault automation. Markdown memory + skills — clone and run with Claude Code or Codex.
- **[brainstorm](https://github.com/kiloloop/brainstorm)** — multi-model brainstorms with 5 copy-paste prompts. Pick a coordinator agent, dispatch to the others, synthesize.
- **[cortex](https://github.com/kiloloop/cortex)** — *archived.* Multi-agent single source of truth that consolidated session debriefs into daily snapshots; superseded by OACP's central debrief store and kept as a reference example.

## Links

- [kiloloop.com](https://kiloloop.com) — company
- [oacp.dev](https://oacp.dev) — protocol docs

## Contact

hello@kiloloop.com
