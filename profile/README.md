<h1><picture><source media="(prefers-color-scheme: dark)" srcset="images/cheapseats-horizontal-dark.svg"><img src="images/cheapseats-horizontal-light.svg" alt="Cheap Seats" width="360"></picture></h1>

Cheap Seats is an AI visibility tracker for Claude and OpenAI models. It asks your buyers'
questions, grades whether answers recommend your product, and ranks pages to improve.
It measures direct model responses rather than consumer apps.

The software is free, MIT licensed and self-hosted. Model access, hosting and optional services
have their own costs. Your prompts live in a git repo you own.

[Live demo](https://demo.cheapseats.dev/) · [Docs](https://cheapseats.dev/docs/)

## Repositories

| Repo | What it is |
| --- | --- |
| [cheapseats](https://github.com/cheapseatsdev/cheapseats) | The app: Go, SQLite, web UI, CLI, JSON API and MCP server. |
| [cheapseats-site](https://github.com/cheapseatsdev/cheapseats-site) | The website, docs and blog at [cheapseats.dev](https://cheapseats.dev). |
| [cheapseats-config-template](https://github.com/cheapseatsdev/cheapseats-config-template) | A template for your deployment's config, prompt sets and workflows. |

## Getting started

With **Go 1.27 or later** and the `claude` CLI installed and logged in, generate a config repo
from your website:

```bash
git clone https://github.com/cheapseatsdev/cheapseats
cd cheapseats
go run ./cmd/cheapseats init https://yoursite.com ../acme-config
# Review ../acme-config TODOs: brand, audience, facts and buyer questions.
CHEAPSEATS_CONFIG=../acme-config/cheapseats.toml go run ./cmd/cheapseats check
CHEAPSEATS_CONFIG=../acme-config/cheapseats.toml go run ./cmd/cheapseats serve
```

Open <http://127.0.0.1:3000>, choose a set and run it. This config uses your Claude subscription
for answers, grading and analysis, with no API key or API spend; calls share your plan's allowance.
OpenAI is optional. [Getting started](https://cheapseats.dev/docs/getting-started/) covers API
setup, and [deployment](https://cheapseats.dev/docs/deploying/) covers containers and VMs.

## Links

[Latest release](https://github.com/cheapseatsdev/cheapseats/releases/latest) ·
[MIT license](https://github.com/cheapseatsdev/cheapseats/blob/main/LICENSE)
