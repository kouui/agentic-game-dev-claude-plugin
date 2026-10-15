# agentic-game-dev-claude-plugin

A Claude Code plugin marketplace for agentic game development. This repo is only an index (`.claude-plugin/marketplace.json`); each plugin lives in its own repository and is pulled from GitHub.

## Use

```bash
claude plugin marketplace add kouui/agentic-game-dev-claude-plugin
claude plugin install <plugin>@agentic-game-dev-claude-plugin -s user
```

## Plugins

| Plugin | Repository | What it does |
| --- | --- | --- |
| `godot` | [kouui/godot-skill-lite](https://github.com/kouui/godot-skill-lite) | Godot 4.7 game building: `godot-game-builder` subagent plus a private skill with dispatcher, lint, scenario and export tools |
| `unity-headless-cli` | [kouui/unity-headless-cli-plugin](https://github.com/kouui/unity-headless-cli-plugin) | Drive a Unity Editor headless from the terminal (fork of the upstream project) |

## Add a plugin

Add an entry to `plugins` in `.claude-plugin/marketplace.json`:

```json
{
  "name": "<plugin-name>",
  "description": "...",
  "source": { "source": "github", "repo": "kouui/<repo>" }
}
```

The plugin repo needs its own `.claude-plugin/plugin.json`.
