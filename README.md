# My .NET Review

A VS Code agent plugin for focused .NET code reviews. It helps identify bugs, regressions, architecture risks, test gaps, maintainability concerns, and code-quality issues.

## What It Includes

- **My .NET Review agent**: A read-only reviewer for change sets, with access to workspace read and search tools. It prioritizes actionable findings and does not implement fixes unless asked.
- **Code reviewer skill**: Review guidance for best practices, potential bugs, improvements, and security concerns.
- **Microsoft Learn MCP server**: A configured connection to the Microsoft Learn documentation service for documentation lookup.

## Install

In VS Code, open the Command Palette and run **Chat: Install Plugin From Source**. Enter this repository's Git URL and follow the prompts.

To use a local checkout, add its path to the `chat.pluginLocations` setting in your user or workspace `settings.json`:

```json
{
  "chat.pluginLocations": {
    "C:/path/to/my-dotnet-review": true
  }
}
```

## Use

Choose **My .NET Review** from the agent picker and ask it to review the current changes or a specific set of files. The reviewer returns findings first, ordered by severity, with file and line references, assumptions, and test gaps. It keeps the review focused on the requested change and its direct dependencies.

The `code-reviewer` skill is available for review and code-quality analysis requests. The Microsoft Learn MCP server provides access to relevant Microsoft documentation when needed.
