# DevTools-SmokeTests

Test repository for Apiiro DevTools inventory smoke tests.
Contains configuration files for IDE, MCP, AI agent, plugin, extension, and skill detection.

**Do not modify** without updating corresponding smoke tests.

## Entity Coverage

| Entity Type  | Sources |
|---|---|
| Ide          | .cursor, .vscode, .idea, .vs, .windsurf |
| IdeExtension | .vscode, .idea, .vs, .windsurf, .cursor (extensions.json in each) |
| AiAgent      | .cursor, .claude, .github, .codex, .gemini |
| McpServer    | .cursor/mcp.json, .vscode/mcp.json, mcp-tools.toml, plugins/formatter/.mcp.json |
| AgentSkill   | .cursor, .claude, .github, .codex, .gemini, lib/ai-skills, plugins/formatter/skills |
| AgentPlugin  | see below |

## Agent plugin sources

Two generations of collectors read this repository, so both fixture shapes are present:

| Generation | Sources | Plugins |
|---|---|---|
| Current collector | .claude/settings.json and .github/copilot/settings.json (enabledPlugins declarations), plugins/formatter/.claude-plugin/plugin.json (vendor-anchored manifest) | cursor-tab, web-search, code-execution (disabled), docs-helper, formatter |
| Legacy collector | .claude/plugins.json, .codex/config.toml, .gemini/extension.yaml, .cursor/extensions.json | cursor-tab, web-search, and others |

Each generation ignores the other's files, and the declared names in both satisfy the same
smoke-suite expectations (at least three plugins, including cursor-tab and web-search).
Remove the legacy files only after every environment runs the current collector.
