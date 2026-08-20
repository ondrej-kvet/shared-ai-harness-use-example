# shared-ai-harness-use-example

Example repository for using the shared AI harness defined in [https://github.com/ondrej-kvet/shared-ai-harness-example](https://github.com/ondrej-kvet/shared-ai-harness-example).

## Prerequisites

uv Python package manager is required to run the MCP server (uv has to be registered in the system PATH). The installation guide is available at [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/). If you don't want to test the MCP server, you can skip this step.

## Installation in different clients

### Claude CLI

The Claude marketplace and plugin is configured in the `.claude/settings.json` file. The plugin is also automatically enabled.

To test the plugin, run claude and check that the plugin in installed with the `/plugins` command. Then you can instruct the agent to test the plugin skill and the MCP server.

### VS Code (Copilot)

The agent standard plugin is configured in `.github/copilot/settings.json` file. VS Code will prompt the user to install the plugin the first time a chat session is opened.

Prerequisite: Agent plugins must be enabled in VS Code settings: `"chat.plugins.enabled": true`.
Note: The current version of VS Code 1.133.0 doesn't support automatic MCP registration from the plugin. The server must be registered manually in VS Code User Settings (`github.copilot.chat.mcp.servers`).

To test the plugin, open this repository in VS Code, open a chat session, and check that the plugin is installed with the `/plugins` command. Then you can instruct the agent to test the plugin skill.

### Copilot CLI

Copilot CLI supports the same configuration path as Claude, so it is using the same `.claude/settings.json` file. The plugin is also automatically enabled (with working MCP).

### Codex CLI and ChatGPT desktop app

The plugin marketplace is configured in `.agents/plugins/marketplace.json`. This file is used by both Codex CLI and ChatGPT desktop app.

To test the plugin, run `codex` in this repository, open the plugin browser with `/plugins`, and install the plugin from the _Repository Codex Plugins_ marketplace. Then start a new session and instruct the agent to test the plugin skill and the MCP server.
