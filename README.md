# agent-sdk-internals

Contributor-facing internals documentation for [Lousho — TypeScript AI agent SDK](https://github.com/LinuxDevil/agent-sdk) (`@lousho/build-ai-agent`).

The [user docs](https://lousho.com/introduction) teach using the SDK. This site teaches **changing** it: every subsystem's entry points, control flow, data flow, and the design decisions behind them — the why, the vision, the how, and the where.

## What's inside

- **Start here** — architecture overview, repo map, dev workflow (clone → green).
- **The run loop** — execution loop, run lifecycle, streaming events, durable execution, error model.
- **Safety and control** — approvals, permission modes, hooks.
- **State and context** — sessions, storage stores, memory, compaction, context assembly.
- **Providers and models** — provider abstraction, model spec resolution, ai-sdk v4–v7 compat, Pi routing, `decide()`, structured output, reasoning.
- **Tools** — tool system, workspace/fs/shell, hosted tools, MCP, OpenAPI, tool search, code mode.
- **Compose agents** — sub-agents, handoffs, flows, skills, agent directories, `.claude/` projects.
- **Interfaces** — server/routes, UI bindings, channels, triggers/schedules, ACP, auth, OAuth.
- **Ship and distribute** — CLI, build targets, spec files, registry kits, `create-lousho-agent`.
- **Techniques** — the prompting/context/agentic catalog mapped to internals: wave engineering, phase engineering, typed decisions.
- **Design decisions** — ADR-style pages: durable-by-default, error codes, branded types, peer-dependency strategy, typed decisions, flow-vs-loop.
- **Quality gates** — mock model, record/replay cassettes, evals, observability, docs pipeline, API report + fallow.
- **Contribute** — adding a feature, code conventions, release process.
- **Study guide** — per-subsystem concept checklist, full glossary, and a no-peeking self-check quiz.

Every subsystem page ends with real `src/` file and symbol references so you can jump straight into the code.

## Developing

```bash
npm i -g mint      # or: npx mint
mint dev           # local preview
mint broken-links  # link check
mint validate      # build validation
```

Pages are hand-written `.mdx`; `docs.json` holds the navigation. When you add a page, add it to `docs.json` and keep the section structure: opening paragraph → Entry points → How it works → Design decisions → Example → Where next.
