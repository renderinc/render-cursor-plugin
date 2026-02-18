# Render

Cursor plugin for deploying, debugging, and monitoring applications on [Render](https://render.com).

## Included

- `rules/`: Render best practices and render.yaml validation checklist
- `skills/`: Deploy, debug, and monitor skills (synced from [render-oss/skills](https://github.com/render-oss/skills))
- `agents/`: Render deployment assistant
- `commands/`: Deploy to Render and check service status
- `mcp.json`: Render MCP server configuration
- `hooks/`: Validates render.yaml after edits

## Skills sync

Skills in `skills/` are synced automatically from the [render-oss/skills](https://github.com/render-oss/skills) repository. A GitHub Action runs daily and opens a PR when changes are detected. To sync manually:

```bash
./scripts/sync-skills.sh
```
