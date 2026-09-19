# BitsWeave Cursor plugin

Thin Agent Plugins package that connects [Cursor](https://cursor.com) to the
BitsWeave Streamable HTTP MCP server at `https://bitsweave.com/api/mcp`.

This repository is a **standalone public shell** — manifests and logo only.
It does not contain BitsWeave server source, API keys, or private monorepo paths.

## What it does

- Registers an MCP server named `bitsweave`
- Lets the agent read and write shared BitsWeave context and work records
- Uses OAuth on first connect (no secrets in this package)

## Install from the Cursor Marketplace

Once this plugin is listed:

1. Open **Cursor → Customize → Plugins** (or browse [cursor.com/marketplace](https://cursor.com/marketplace))
2. Search for **BitsWeave** / `bitsweave`
3. Install and enable the plugin
4. On the first BitsWeave tool call, complete the BitsWeave login (OAuth) in the browser

Until marketplace listing is live, use the local smoke path below.

## Local smoke test

```bash
# From a clone of this repo (or copy of its root):
mkdir -p ~/.cursor/plugins/local
ln -sfn "$(pwd)" ~/.cursor/plugins/local/bitsweave
```

Restart Cursor. Open **Customize** and confirm the plugin exposes the `bitsweave`
MCP server. Call any BitsWeave tool and finish the OAuth login when prompted.

To unlink:

```bash
rm ~/.cursor/plugins/local/bitsweave
```

## Auth note

The first MCP tool call starts the BitsWeave OAuth flow. This package never
ships a token or PAT — credentials stay in your Cursor / BitsWeave session.

## Layout

```
.
├── plugin.json       # Agent Plugins manifest (name: bitsweave)
├── mcp.json          # url-only MCP server entry
├── assets/logo.svg   # BitsWeave logo (relative path in manifest)
├── LICENSE           # MIT
└── README.md
```

## Marketplace submit (owner)

After local smoke passes, submit the public repo URL at
[cursor.com/marketplace/publish](https://cursor.com/marketplace/publish).

Optional community listing:
[cursor.directory/plugins/new](https://cursor.directory/plugins/new)

## Links

- Product: [bitsweave.com](https://bitsweave.com)
- Repository: [github.com/kirchoff-digital/bitsweave-cursor-plugin](https://github.com/kirchoff-digital/bitsweave-cursor-plugin)
