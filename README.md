<div align="center">

# renovate-config

[![CI](https://img.shields.io/github/actions/workflow/status/itsmelouis/renovate-config/ci.yml?style=flat-square&logo=github&label=CI)](https://github.com/itsmelouis/renovate-config/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](./LICENSE)
[![Renovate](https://img.shields.io/badge/preset-Renovate-1A1F6C?style=flat-square&logo=renovate&labelColor=1A1F6C)](https://docs.renovatebot.com)

My shared [Renovate](https://github.com/renovatebot/renovate) preset - calm, grouped and secure dependency updates.

[Usage](#usage) • [What It Does](#what-it-does) • [Development](#development)

</div>

## Usage

Add this to your `renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>itsmelouis/renovate-config"]
}
```

## What It Does

- **Weekend schedule** - PRs and lockfile maintenance only on weekends
- **Grouped updates** - all minor/patch updates in one PR, majors in their own
- **Ecosystem groups** - `nuxt framework`, `cloudflare` and `lint and format` stay together, majors included
- **Release age** - waits 24 hours before proposing a new version
- **Ranges** - bumps ranges (`^1.2.0` → `^1.3.0`) and runs `pnpm dedupe`
- **Pinned actions** - GitHub Actions pinned to commit digests
- **Security first** - vulnerability fixes skip the schedule, labeled `security`
- **Commits** - `chore` semantic commits with a `Co-authored-by` trailer

## Development

Requires [Node.js](https://nodejs.org) and [pnpm](https://pnpm.io).

```bash
pnpm install      # Install the dependencies
pnpm test         # Validate the config with renovate-config-validator
```

## License

MIT © [Louis F.](https://github.com/itsmelouis)
