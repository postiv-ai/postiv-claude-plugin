# Postiv for Claude

A Claude plugin combining the Postiv MCP connector with a content skill and five guided playbooks.

Create posts, carousels, infographics, and images. Schedule content, reply to comments, and track what works across LinkedIn personal profiles and company pages in your connected workspace.

## Connect

Install the plugin in a Claude client that supports plugins. Authenticate the Postiv connector when prompted: sign in to your Postiv account, choose a workspace, and approve read-only or read-and-write access. The remote MCP server is https://postiv.ai/mcp. No API key or client secret is bundled in this repository.

A Postiv account and workspace access are required. Connect the relevant LinkedIn profiles in Postiv for publishing, comments, and analytics. Each OAuth connection is scoped to the workspace chosen during sign-in. Installing the plugin does not authorize publishing.

## Included workflows

- Interview me about a subject and turn my answers into content.
- Turn meeting transcripts into content answering customer questions. Supply the transcript or use a separately connected meeting recorder.
- Find and repurpose my best-performing posts.
- Draft content from Bob’s existing content plan.
- Adapt the big idea from winning posts in my niche.

The skill loads the relevant playbook as needed. Simple requests can use the MCP tools directly.

## Local validation

```sh
claude plugin validate .
```

For a local Claude Code trial, run `claude --plugin-dir .` from this directory, then authenticate Postiv through Claude’s MCP controls. This repository does not install or run a local MCP server.

## Repository structure

- `.claude-plugin/plugin.json`: plugin metadata and version.
- `.mcp.json`: remote Postiv connection configuration.
- `skills/postiv/SKILL.md`: general instructions and workflow routing.
- `skills/postiv/playbooks/`: five content workflows.

## Updates

Edit the skill and playbooks here, update the version in `.claude-plugin/plugin.json`, and record the change in `CHANGELOG.md` before publishing a release. Distribution and client refresh determine when installed copies update. The hosted MCP service is deployed separately.

## Links

- [Postiv](https://postiv.ai)
- [Connection documentation](https://postiv.ai/api-documentation/hosted-mcp)
- [Support](https://intercom.help/postiv-ai/en)
- [Privacy policy](https://postiv.ai/privacy-policy)

This repository contains the plugin instructions and connection configuration, not the Postiv application source. It has not yet been approved for the Claude directory.
