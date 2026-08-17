# shared-ai-harness-use-example

Example repository for using the shared AI harness defined in [https://github.com/ondrej-kvet/shared-ai-harness-example](https://github.com/ondrej-kvet/shared-ai-harness-example).

## Claude plugin installation

The Claude marketplace and plugin is configured in the `.claude/settings.json` file. The plugin is also automatically enabled.

To test the plugin, run claude and check that the plugin in installed with the `/plugins` command. Then you can instruct the agent to test the plugin skill and the MCP server.

## Agent standard plugin installation

### Copilot in VS Code

The agent standard plugin is configured in `.github/copilot/settings.json` file. VS Code will prompt the user to install the plugin the first time a chat session is opened.

Prerequisite: Agent plugins must be enabled in VS Code settings: `"chat.plugins.enabled": true`.
Note: The current version of VS Code 1.133.0 doesn't support automatic MCP registration from the plugin. The server must be registered manually in VS Code User Settings (`github.copilot.chat.mcp.servers`).

To test the plugin, open this repository in VS Code, open a chat session, and check that the plugin is installed with the `/plugins` command. Then you can instruct the agent to test the plugin skill.

### Copilot CLI

Copilot CLI supports the same configuration path as Claude, so it is using the same `.claude/settings.json` file. The plugin is also automatically enabled (with working MCP).

### Codex CLI

TODO
