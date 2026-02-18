---
name: deploy-to-render
description: Deploy the current project to Render by analyzing the codebase, generating a render.yaml Blueprint, and providing a Dashboard deeplink.
---

# Deploy to Render

1. Analyze the codebase to determine framework, runtime, build/start commands, environment variables, and datastores.
2. Generate a `render.yaml` Blueprint with the appropriate services and databases.
3. Validate the Blueprint with `render blueprints validate` if the CLI is installed.
4. Commit and push the `render.yaml` to the repository.
5. Provide a Dashboard deeplink: `https://dashboard.render.com/blueprint/new?repo=<REPO_URL>`.
6. Remind the user to fill in secret environment variables marked with `sync: false`.
