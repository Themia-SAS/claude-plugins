# Themia — Claude Code plugin marketplace

The `themia` marketplace catalog. Org-level registry for Themia's internal Claude Code plugins. Private; internal team only.

This repo holds **only** the marketplace catalog (`.claude-plugin/marketplace.json`). Each plugin lives in its own repo and is referenced here as a github source.

## Plugins

| Plugin | Repo | Role |
|---|---|---|
| `jurimetria-lab` | [`Themia-SAS/jurimetria-lab`](https://github.com/Themia-SAS/jurimetria-lab) | **Produces** the verified jurimetric truth — research + verification skills/agents, MCP-bound. |
| `croissance-lab` | [`Themia-SAS/croissance-lab`](https://github.com/Themia-SAS/croissance-lab) | **Distributes** it — growth: copy, webinar, (roadmap) LinkedIn / outreach / campaign agent. |

## Install

```bash
/plugin marketplace add Themia-SAS/claude-plugins   # add the `themia` catalog (one-time)
/plugin install jurimetria-lab@themia
/plugin install croissance-lab@themia
/plugin update <name>
```

## Adding a plugin to the catalog

1. Ship the plugin in its own `Themia-SAS/<name>` repo (with `plugin.json`).
2. Add an entry to `.claude-plugin/marketplace.json` here (name + github source + description).
3. Users run `/plugin marketplace update themia` to see it.

Note: each plugin bumps its **own** `plugin.json` version on release — `/plugin update` checks that, not this catalog.
