# Render

Cursor plugin for deploying, debugging, and monitoring applications on [Render](https://render.com).

## Included

- `rules/`: Render best practices and render.yaml validation checklist
- `skills/`: Deploy, debug, and monitor skills (synced from [render-oss/skills](https://github.com/render-oss/skills))
- `agents/`: Render deployment assistant
- `commands/`: Deploy to Render and check service status
- `.mcp.json`: Render MCP server configuration (OAuth via the pre-registered Cursor client)
- `hooks/`: Validates render.yaml after edits

## Render MCP in Cursor

This plugin declares the hosted Render MCP server in `.mcp.json` with the pre-registered Cursor OAuth client id `cursor`. After installing or updating the plugin, Cursor connects to `https://mcp.render.com/mcp` and prompts for Render OAuth the first time MCP tools are used.

No `RENDER_API_KEY` or manual `~/.cursor/mcp.json` entry is needed for the plugin-provided MCP connection. Manual API-key setup is still useful for other AI tools or the Render CLI fallback.

## Skills sync

Skills in `skills/` are synced automatically from the [render-oss/skills](https://github.com/render-oss/skills) repository. A GitHub Action runs daily and opens a PR when changes are detected. To sync manually:

```bash
./scripts/sync-skills.sh
```
