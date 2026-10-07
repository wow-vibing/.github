# wow-vibing

Tooling and custom content for **World of Warcraft: Wrath of the Lich King 3.3.5a (build 12340)** private-server modding,
built on [AzerothCore](https://github.com/azerothcore/azerothcore-wotlk) and its Lua engine [mod-ale](https://github.com/azerothcore/mod-ale).

## Repositories (members)

| Repo | What |
|---|---|
| `wow-dev` | The workspace: raid encounters (Lua), designs, client patch staging; pins every tool below |
| `wdbc-tools` | Generic WDBC (.dbc) row clone/edit/verify CLI, a byte-exact writer validated with DBCD + WoWDBDefs |
| `wow-asset-pipeline` | `wowap` CLI: audio convert/verify, DBC inspection, patch validation, MPQ build |
| `acore-dev-env` | Reproducible AzerothCore + mod-ale docker environment: pinned versions, overlays, deploy/restart scripts |
| `claude-wow-plugin` | Claude Code plugin: modding skills, specialised agents and safety hooks |
| `wow-docs` | Documentation site (MkDocs, WoW-inspired theme) covering the toolchain, pipelines and raids |

## Focus
- **Raid encounters first**: 10- and 25-player bosses scripted in Lua (mod-ale), starting with a one-boss Orgrimmar arena raid
- **Client asset pipeline**: custom audio → DBC rows → MPQ client patches
- **AI-assisted workflow** with [Claude Code](https://claude.com/claude-code), guarded by hooks that block destructive and secret-leaking actions

Repositories are private to members. No Blizzard game files are distributed by this organization.
