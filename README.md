# design-skills

Personal Claude plugin marketplace. Each entry points to a repository that holds the skills; nothing is copied here.

## Plugins

| Plugin | Source | Contents |
|---|---|---|
| `emil-design-eng` | [Thibault-Grondin-B/emil-skills](https://github.com/Thibault-Grondin-B/emil-skills), a fork of [emilkowalski/skills](https://github.com/emilkowalski/skills) (MIT) | Animation, motion and UI craft skills by Emil Kowalski |

The fork exists only to add `.claude-plugin/plugin.json`, which claude.ai requires and the original repo does not have. To pull Emil's latest changes, click **Sync fork** on the fork's GitHub page.

## Add to Claude

Customize > Plugins > + > Add marketplace > Add from a repository, then paste:

```
https://github.com/Thibault-Grondin-B/design-skills
```

## Add another plugin

Append an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "plugin-name",
  "description": "What it does",
  "source": { "source": "github", "repo": "owner/repo" }
}
```

The source repo must be public and contain a `skills/` folder (one subfolder per skill, each with a `SKILL.md`) or its own `.claude-plugin/plugin.json`.
