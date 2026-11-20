# design-skills

Personal Claude plugin marketplace. It does not copy any skills: each entry points to the original repository, so updates from the authors sync automatically.

## Plugins

| Plugin | Source | Contents |
|---|---|---|
| `emil-design-eng` | [emilkowalski/skills](https://github.com/emilkowalski/skills) (MIT) | Animation, motion and UI craft skills by Emil Kowalski |

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
