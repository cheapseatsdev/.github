<h1><picture><source media="(prefers-color-scheme: dark)" srcset="images/cheapseats-horizontal-dark.svg"><img src="images/cheapseats-horizontal-light.svg" alt="Cheap Seats" width="360"></picture></h1>

Cheap Seats is an open-source (MIT) AI visibility tracker. It asks your buyers' questions of AI
assistants, grades whether they recommend you, and builds a ranked list of fixes, running on the
Claude subscription you already have (ChatGPT optional). It's free, and always will be: no hosted
tier, no upsell.

- Asks each buyer question of Claude and ChatGPT, through their APIs or the `claude` and `codex`
  CLIs on your subscriptions, on two tracks: **search** (what the web says today) and **recall**
  (what the model already believes).
- Grades every answer `recommended`, `mentioned` or `absent`, and records your position, the top
  pick, every product named, objections, and every search result and citation.
- Ends each run with **Fix these first**: the exact page to create or change, what it must say and
  the prompts it should flip. **Quick wins** ranks fixes across all your prompt sets.
- Trends each set week to week, and runs free checks beside it: what AI crawlers can read on your
  sites, and which cited pages name you.
- Self-hosted: Docker, Kubernetes (Helm chart) or a VM. Web UI, CLI, JSON API and MCP server. Your
  prompts live in a git repo you own.

## Getting started

With Go 1.25+ and the `claude` CLI logged in (no API key needed), start a config repo from your
website:

```bash
git clone https://github.com/cheapseatsdev/cheapseats && cd cheapseats
go run ./cmd/cheapseats init https://yoursite.com ../acme-config   # -dry-run to see it first
CHEAPSEATS_CONFIG=../acme-config/cheapseats.toml go run ./cmd/cheapseats serve
```

Or start from the [config template](https://github.com/cheapseatsdev/cheapseats-config-template).
The full walkthrough is in [Getting started](https://cheapseats.dev/docs/getting-started/).

## Repositories

| Repo | What it is |
| --- | --- |
| [cheapseats](https://github.com/cheapseatsdev/cheapseats) | The app (Go, SQLite). Image `ghcr.io/cheapseatsdev/cheapseats`, Helm chart `oci://ghcr.io/cheapseatsdev/charts/cheapseats`. |
| [cheapseats-site](https://github.com/cheapseatsdev/cheapseats-site) | The website, docs and blog at [cheapseats.dev](https://cheapseats.dev). |
| [cheapseats-config-template](https://github.com/cheapseatsdev/cheapseats-config-template) | A template for starting a deployment: config, prompt sets and deploy workflows. |

## Links

[Site](https://cheapseats.dev) ·
[Docs](https://cheapseats.dev/docs/) ·
[Latest release](https://github.com/cheapseatsdev/cheapseats/releases/latest) ·
[MIT license](https://github.com/cheapseatsdev/cheapseats/blob/main/LICENSE)
