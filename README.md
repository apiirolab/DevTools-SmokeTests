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
| McpServer    | .cursor/mcp.json, .vscode/mcp.json, mcp-tools.toml |
| AgentSkill   | .cursor, .claude, .github, .codex, .gemini, lib/ai-skills |
| AgentPlugin  | .cursor (JSON), .claude (JSON), .codex (TOML), .gemini (YAML) |
