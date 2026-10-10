# wow-vibing

Tooling and custom content for **World of Warcraft: Wrath of the Lich King 3.3.5a (build 12340)** private-server modding,
built on [AzerothCore](https://github.com/azerothcore/azerothcore-wotlk) and its Lua engine [mod-ale](https://github.com/azerothcore/mod-ale).

## Repositories (members)

| Repo | Use it for |
|---|---|
| `wow-dev` | The workspace: raid encounters (Lua), designs, client patch staging, docs; pins every tool below. **Start here** |
| `wowmod-toolkit` | `wowmod`, the orchestrator CLI: one command per modding process (creature looks, sounds, items, spells, maps and entrances, loot, SQL with revert) |
| `wdbc-tools` | `wdbc`, the DBC engine: read, clone and edit rows of any 3.3.5a `.dbc` into new, verified files |
| `wow-asset-pipeline` | `wowap`, the asset engine: audio conversion and checks, patch staging, MPQ build |
| `acore-dev-env` | The server environment: pinned AzerothCore + mod-ale, Lua deploy, restart, logs, safe SQL read/apply |
| `claude-wow-plugin` | Claude Code plugin: skills that map tasks to the commands above, specialised agents, safety hooks |
| `wow-docs` | Documentation site (MkDocs, WoW-inspired theme) built from all of the above |

## How the pieces fit

```text
 knowledge     claude-wow-plugin (skills, agents, hooks) · docs · wow-docs
     │
 orchestrator  wowmod  ── one command per process, writes reviewable outputs only
     │
 engines       wdbc · wowap                     server env   acore-dev-env
     │                                                │
 runtime       client patch (MPQ)                      AzerothCore + mod-ale (docker)
```

Every CLI shares one contract: `--json` output and exit codes `0` ok, `1` check failed, `2` usage, `3` refused, `4` environment.

## Getting started (members)

1. `wow-dev` → `docs/onboarding.md` (clone, `./bootstrap.sh`, your first hour)
2. `wow-dev` → `docs/architecture/toolchain.md` (which tool for which task, worked examples)
3. The README of the tool you need

## Focus
- **Raid encounters first**: 10- and 25-player bosses scripted in Lua (mod-ale)
- **Client content pipeline**: DBC rows, audio, textures and maps → MPQ client patches, with matching server rows
- **AI-assisted workflow** with [Claude Code](https://claude.com/claude-code), guarded by hooks that block destructive and secret-leaking actions

Repositories are private to members. No Blizzard game files are distributed by this organization.
