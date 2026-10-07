# Contributing to wow-vibing

Thanks for helping! These rules apply to every repository in the organization unless a repository has its own `CONTRIBUTING.md`.

## Workflow
1. Open or pick an issue (use the templates: encounter request, sound request, bug report).
2. Create a branch: `git switch -c <type>/<short-topic>` (e.g. `feat/boss-9000001`, `fix/sound-90001-path`).
3. Run the repository's bootstrap once per clone (`./bootstrap.sh --apply` in `wow-dev`): it enables the git hooks.
4. Commit in small steps with clear messages (`feat:`, `fix:`, `docs:`, `chore:`).
5. Push your branch and open a pull request. Fill in the checklist in the PR template.
6. A member of **@wow-vibing/maintainers** reviews every PR. Squash-merge once approved; the branch is deleted automatically.

Direct pushes to `main` are not allowed (enforced by local hooks and by review: our private repos have no server-side branch protection).

## Ground rules
- **Never commit Blizzard client files** (DBC, MPQ, ADT, BLP, M2, extracted data) or other copyrighted assets you don't have rights to.
- **Never commit secrets** (tokens, `.env` files, passwords). If you leak one, follow [SECURITY.md](SECURITY.md) immediately.
- Don't delete other people's work or remote branches. Propose removals in an issue or PR.
- Upstream projects (AzerothCore, mod-ale, DBCD, WoWDBDefs) are pinned, not modified. Changes to them start as an issue.

## Using AI assistants
AI-generated changes follow the same rules and review as human ones. The `wow-dev` repository ships a Claude Code configuration
(`CLAUDE.md`, `.claude/`) with safety hooks. Don't weaken them in shared settings; use `.claude/settings.local.json` for personal preferences.
