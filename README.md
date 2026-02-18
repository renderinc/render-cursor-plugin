# Render Cursor Plugins

Cursor Marketplace plugins for deploying, debugging, and monitoring applications on [Render](https://render.com).

## Plugins

- **render**: Rules, skills, agents, commands, hooks, and MCP config for the full Render workflow. See [`plugins/render/README.md`](plugins/render/README.md).

## Skills sync

Skills in `plugins/render/skills/` are synced automatically from [render-oss/skills](https://github.com/render-oss/skills). A GitHub Action runs daily and opens a PR when changes are detected. To sync manually:

```bash
./scripts/sync-skills.sh
```

## Adding plugins

To add more plugins, see [`docs/add-a-plugin.md`](docs/add-a-plugin.md).

## Validation

```bash
node scripts/validate-template.mjs
```

## Submission checklist

- Each plugin has a valid `.cursor-plugin/plugin.json`.
- Plugin names are unique, lowercase, and kebab-case.
- `.cursor-plugin/marketplace.json` entries map to real plugin folders.
- All frontmatter metadata is present in rule, skill, agent, and command files.
- Logos are committed and referenced with relative paths.
- `node scripts/validate-template.mjs` passes.
