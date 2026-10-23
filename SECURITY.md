# Security policy

Cheap Seats runs on your own machine or VM against your own API keys and model subscriptions, and
it sends prompts and answers only to the model providers you configure. A security problem in it is
one in yours, so we want to hear about it quickly and quietly.

## Reporting a vulnerability

Use GitHub's private vulnerability reporting on the repository concerned
([cheapseats](https://github.com/cheapseatsdev/cheapseats/security/advisories/new) for the app,
[cheapseats-site](https://github.com/cheapseatsdev/cheapseats-site/security/advisories/new) for the
website). The report stays private between you and the maintainer until a fix is out. Please do not
open a public issue for anything that could be a vulnerability.

Include what you found, how to reproduce it, and what you think the impact is. You will hear back
within a few days, and the advisory is where the discussion and the fix are tracked.

## What is in scope

- The `cheapseats` binary, image and Helm chart: the web UI, the JSON API, the MCP server, the CLI,
  the answerers, the grader, the site audit and citation checks, and the exe.dev deploy scripts.
- cheapseats.dev and demo.cheapseats.dev.

Out of scope: the model providers themselves, and findings that need a compromised machine or a
stolen token to begin with (treat those as "rotate the token").

## Supported versions

The latest release on the [releases page](https://github.com/cheapseatsdev/cheapseats/releases).
Fixes ship as a new release; there are no backports.
