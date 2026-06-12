# AI Architect — Cursor Plugin

A [Cursor Marketplace plugin](https://cursor.com/marketplace) that connects
Cursor to [Atsign AI Architect](https://aiarchitect.atsign.com) via MCP
(Model Context Protocol).

AI Architect is a no code drag and drop web application that allows you to design "blueprints" that show the design and dataflows within your application or system in plain language.
Once you are happy with the blueprint then you can export a prompt that includes all the skills needed to build the application, agents and APIs to bring the blueprint to life on the Atsign Platform. The Atsign Platform provides secure communications between components with no network attack surfaces. 
 Applications and agents that are built using Atsign AI Architect can run on Windows, Mac, IoS, Android and Linux.  

## What this plugin does

Registers the `aiarchitect` MCP server so Cursor agents can interact with
AI Architect tools directly from the editor. Once installed, Cursor will
connect to `https://aiarchitect.atsign.com/mcp` over SSE and expose all
available AI Architect tools to the agent.

## Prerequisites

An [AI Architect account](https://aiarchitect.atsign.com). Sign up at
<https://aiarchitect.atsign.com>.

## Installation

Install via the Cursor Marketplace or add this repository directly:

1. Open Cursor → **Settings** → **Plugins**
2. Search for **aiarchitect** or **Atsign**
3. Enable the plugin — the MCP server connects automatically

## MCP server

| Field     | Value                                 |
|-----------|---------------------------------------|
| Name      | `aiarchitect`                         |
| URL       | `https://aiarchitect.atsign.com/mcp` |
| Transport | SSE (Server-Sent Events)              |

> **Note:** The MCP server at `https://aiarchitect.atsign.com/mcp` requires an
> active AI Architect session. Users must be signed in to their account at
> [aiarchitect.atsign.com](https://aiarchitect.atsign.com) for the connection
> to authenticate successfully.

## Repository structure

```
.cursor-plugin/plugin.json   # Cursor plugin manifest
mcp.json                     # MCP server definition
assets/logo.svg              # Plugin logo
README.md
```

## Security

See [SECURITY.md](SECURITY.md).

## License

Apache 2.0 — see [LICENSE](LICENSE).

## Acknowledgement/Attribution

AI Architect and the Atsign brand are trademarks of Atsign Limited.
The plugin logo is sourced from [aiarchitect.atsign.com](https://aiarchitect.atsign.com).

## Maintainers

Maintained by [@cconstab](https://github.com/cconstab).
