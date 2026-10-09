# PowerSEC CLI

Command-line tool for [PowerSEC](https://powersec.io) — start malware scans, check scan
results, and manage alerts across every WordPress site connected to your PowerSEC account,
without opening the dashboard.

## Install

```bash
npm install -g @powersec/cli
```

Requires Node.js 18 or newer.

## First run

Authenticate the CLI with a key from your PowerSEC account
(**Dashboard → Settings → API keys**), then list your sites:

```bash
psec auth login
psec sites list
```

## Common commands

```bash
# Start a malware scan and wait for it to finish
psec scan run example.com --wait

# Show the result of the last scan
psec scan status --site example.com

# List open alerts across every site
psec alerts list --status open

# List resolved alerts for one site
psec alerts list --status resolved --site 12345
```

`--site` accepts either a domain (`example.com`) or a site ID (`12345`).

## Why use the CLI

- **Fleet-wide, scriptable checks** — put a scan or an alert sweep into cron or CI.
- **No browser** — works over SSH, in containers, and on servers with no dashboard access.
- **Same account, same data** — the CLI reads the same sites, scans, and alerts as PowerSEC Central.

## Links

- Product: <https://powersec.io>
- Changelog: <https://powersec.io/changelog>
- WordPress plugin: <https://wordpress.org/plugins/powersec/>
- Help center / API recipes: <https://powersec.io/help>
- npm: <https://www.npmjs.com/package/@powersec/cli>

## About

Built by [CinderEye LLC](https://powersec.io/about). PowerSEC is WordPress security
monitoring with an open-source firewall, malware scanner, login protection and backup
plugin, plus an optional central dashboard for managing many sites.

---

*This repository is the public home of the PowerSEC CLI: documentation, release notes and
issue tracking. The CLI is distributed through npm.*
