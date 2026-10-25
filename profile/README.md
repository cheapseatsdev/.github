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

Choose the path that matches your model access:

| Path | What you need | Model costs |
| --- | --- | --- |
| [Docker with API keys](https://cheapseats.dev/docs/getting-started/#docker-with-api-keys) — fastest setup | Docker and `ANTHROPIC_API_KEY`; `OPENAI_API_KEY` is optional. No Go or CLI installation. | Paid API usage. |
| [Go with subscriptions](https://cheapseats.dev/docs/getting-started/#go-with-subscriptions) | Go 1.27+ and an installed, logged-in `claude` CLI; `codex` is optional. | No API spend; calls share your subscription allowance. |

The Docker image includes neither subscription CLI. See [deployment](https://cheapseats.dev/docs/deploying/)
for containers and VMs.

## Links

[Latest release](https://github.com/cheapseatsdev/cheapseats/releases/latest) ·
[MIT license](https://github.com/cheapseatsdev/cheapseats/blob/main/LICENSE)
