# Kiloloop

**Run a fleet of AI coding agents — portable, auditable, human-in-command.**

Kiloloop builds vendor-neutral tools for one loop: **plan** delegated AI work, **coordinate** it, and **learn** from every run. Coordination lives in plain files (no server), messages are signed and verifiable, and agents declare their scope up front — when a run drifts from its declaration, the protocol pauses it for a human. Everything here is maintained daily by the agent fleet it coordinates — the same protocol these repos document is the one that ships them.

## Products

- **[OACP](https://github.com/kiloloop/oacp)** — the Open Agent Coordination Protocol. Typed async messaging between agents (task dispatch, code review, handoff, brainstorm) plus persistent shared memory across agents, projects, and machines. File-based and runtime-agnostic: Claude Code, Codex, Gemini, or anything that reads YAML. Agents declare minutes, files, and side effects before work starts; mid-run checkpoints pause for human re-authorization when reality drifts from the declaration. v0.4 adds Ed25519-signed messages and audit records for every autonomy decision. `pip install oacp-cli`

- **[agent-estimate](https://github.com/kiloloop/agent-estimate)** — know what an AI task will cost before you run it, and how the forecast held up after. PERT estimates calibrated for AI agents, human-equivalent compression ratios, METR reliability thresholds, and multi-agent wave planning. CLI, GitHub Action, and Claude Code plugin.

## Tools and skills

Drop-in pieces for your agent runtime, dogfooded daily by the fleet that maintains these repos:

- **[oacp-skills](https://github.com/kiloloop/oacp-skills)** — reusable skills for OACP agents: check-inbox, doctor, review-loop, self-improve, wrap-up.
- **[memory-lint](https://github.com/kiloloop/memory-lint)** — deterministic linter for AI agent memory files: broken wiki-links, index drift, stale entries, malformed frontmatter. Run it by hand or drop it in CI. `pip install memory-lint`
- **[kiloloop-skills](https://github.com/kiloloop/kiloloop-skills)** — agent-discipline skills for coding-agent runtimes (Claude Code, Codex): self-contained, versioned, fixture-tested. First skills are on the way, starting with a memory-lint wrapper.

## Reference workflows

Working examples you can fork, built on the products above:

- **[iantha](https://github.com/kiloloop/iantha)** — a personal chief of staff. Morning briefings, evening reviews, decision logs, optional Obsidian vault automation. Markdown memory + skills — clone and run with Claude Code or Codex.
- **[brainstorm](https://github.com/kiloloop/brainstorm)** — multi-model brainstorms with 5 copy-paste prompts. Pick a coordinator agent, dispatch to the others, synthesize.
- **[cortex](https://github.com/kiloloop/cortex)** — multi-agent single source of truth; consolidates session debriefs into daily snapshots.

## Links

- [kiloloop.com](https://kiloloop.com) — company
- [oacp.dev](https://oacp.dev) — protocol docs

## Contact

hello@kiloloop.com
