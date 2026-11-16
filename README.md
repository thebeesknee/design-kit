# design-kit

My Claude Code plugin marketplace for web and Shopify design work. One repo, shared by my
personal and work Claude setups.

| Plugin | What it does | Source |
|---|---|---|
| `design-references` | My library of DESIGN.md style references | This repo, `plugins/design-references` |
| `impeccable` | Design, critique, audit, polish and animate frontends | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) |
| `taste-skill` | Professional company websites, checked in a real browser | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |

The third-party plugins are only *listed* here and are installed from their authors' repos,
so they keep receiving updates.

## Install on a machine

In Claude Code:

```
/plugin marketplace add <github-user>/design-kit
/plugin install design-references@design-kit
/plugin install impeccable@design-kit
/plugin install taste-skill@design-kit
```

If impeccable or taste-skill is already installed from its own marketplace, either keep that
copy or uninstall it first so you don't run two copies.

## Get updates

```
/plugin marketplace update design-kit
```

## Add a design reference

1. Save the DESIGN.md as
   `plugins/design-references/skills/design-references/references/<style-name>.md`.
2. Add a row to the Library table in that folder's `SKILL.md`.
3. Bump `version` in `plugins/design-references/.claude-plugin/plugin.json` and in
   `.claude-plugin/marketplace.json`, then commit and push.

Or ask Claude: "add this DESIGN.md to my design-references library" (with the link or file).

## Add another plugin or skill

- **Your own skill:** create `plugins/<name>/.claude-plugin/plugin.json` and
  `plugins/<name>/skills/<name>/SKILL.md`, then add an entry with
  `"source": "./plugins/<name>"` to `marketplace.json`.
- **Someone else's plugin:** add an entry whose `source` points at their GitHub repo, as the
  impeccable and taste-skill entries do.
