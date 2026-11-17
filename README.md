# Envisioning foresight skill

This skill lets your AI agent run Envisioning's foresight method. The agent frames a strategic question, scans for signals of change, checks each claim against its sources, places the signals by category, readiness and horizon, checks timing claims against graded past forecasts, and writes a radar with every source cited.

The agent pulls data from Envisioning's open research: thousands of technologies with readiness scores, a technology vocabulary, and Hindsight, a dataset of published forecasts graded against what happened. It cites envisioning.com permalinks for everything it uses from us.

The skill is free and public.

## What is in the repository

- `skills/foresight/SKILL.md`: the method as steps an agent follows.
- `skills/foresight/references/`: the full method with its sources, data sources and citation rules, scan types, the Hindsight check, the output format, and short definitions.
- `.claude-plugin/`: the Claude Code plugin and marketplace manifests.
- `.mcp.json`: the envisioning.com MCP server (`https://www.envisioning.com/mcp`, read-only, no sign-in).

## Install

### Claude Code

In a Claude Code session, run:

```
/plugin marketplace add envisioning/foresight-skill
/plugin install envisioning-foresight@envisioning
```

The plugin adds the skill and connects the envisioning.com MCP server. Ask for a horizon scan, a technology radar or "what is next for" a field, and Claude uses the skill. You can also call it directly with `/envisioning-foresight:foresight`.

### Claude.ai and the Claude desktop app

1. Download this repository and zip the `skills/foresight` folder.
2. In Claude, open Settings, then Capabilities, and upload the zip under Skills.
3. To give Claude the data tools too, add a custom connector with the URL `https://www.envisioning.com/mcp`.

### Other agents

`skills/foresight/SKILL.md` follows the Agent Skills format, so it works in any agent that supports that format. Copy the `skills/foresight` folder to wherever your agent loads skills from. Add `https://www.envisioning.com/mcp` as a remote MCP server (Streamable HTTP). If your agent has no MCP support, the skill tells it how to read the same data from https://www.envisioning.com/llms.txt and from Markdown versions of each page.

## Data the skill uses

- envisioning.com research hubs, technology library and vocabulary
- Hindsight: https://www.envisioning.com/hindsight and https://github.com/envisioning/hindsight
- The National Capability Benchmark: https://ncb.envisioning.com
- The methodology chapters: https://www.envisioning.com/methodology

To run scans continuously across many questions and models, Envisioning Signals runs the same method as a platform: https://signals.envisioning.com

## License

The skill text is CC BY 4.0. The code and configuration are MIT. See `NOTICE.md` and `LICENSE`.

Made by Envisioning, https://www.envisioning.com
