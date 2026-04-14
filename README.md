# T3 Code (Fork with Kimi support)

This is a personal fork of [T3 Code](https://github.com/pingdotgg/t3code) with experimental support for the **Kimi** provider, plus plan-mode fixes and UI improvements.

## What's different in this fork

- **Kimi provider**: Start sessions and send turns using the Kimi CLI (`kimi`).
- **Plan mode support**: Kimi now correctly enters plan mode and renders proposed plans in the UI.
- **Runtime mode UI filter**: "Auto-accept edits" is hidden for Kimi (Kimi only supports `full-access` vs `approval-required`).
- **SDK patch**: Patches `@moonshot-ai/kimi-agent-sdk@0.1.8` to handle the `PlanDisplay` event emitted by the Kimi CLI in plan mode.

## Installation

> [!WARNING]
> This fork is experimental. Install and authenticate at least one provider before use:
>
> - **Codex**: install [Codex CLI](https://github.com/openai/codex) and run `codex login`
> - **Claude**: install Claude Code and run `claude auth login`
> - **Kimi**: install the [Kimi CLI](https://www.moonshot.cn/) and ensure `kimi` is in your `PATH`

### Run from source

```bash
git clone https://github.com/rafaelcg/t3code.git
cd t3code
bun install
bun run dev
```

### Prebuilt releases

There are no prebuilt releases for this fork. If you want a packaged build, you'll need to build it locally (see [CONTRIBUTING.md](./CONTRIBUTING.md) for build steps).

## Some notes

This is a very early WIP fork. Expect bugs.

Upstream is not accepting contributions yet, but this fork exists for personal experimentation.

Observability guide: [docs/observability.md](./docs/observability.md)

## Local development

Before local development, prepare the environment and install dependencies:

```bash
# Optional: only needed if you use mise for dev tool management.
mise install
bun install
```

Read [CONTRIBUTING.md](./CONTRIBUTING.md) before opening an issue or PR.
