# BitsWeave Cursor plugin

Public Cursor marketplace package for the BitsWeave Streamable HTTP MCP server
at `https://bitsweave.com/api/mcp`.

Manifests and logo only — no server source, API keys, or private monorepo paths.

## Install (before official marketplace listing)

1. Cursor → **Customize** → **Plugins** → **Import Marketplace**
2. Repository: `https://github.com/kirchoff-digital/bitsweave-cursor-plugin`
3. Scope: User (or Team)
4. Import, then install **BitsWeave** from the imported marketplace
5. On first BitsWeave tool call, finish OAuth in the browser

## Local symlink smoke (optional)

```bash
mkdir -p ~/.cursor/plugins/local
ln -sfn "$(pwd)/plugins/bitsweave" ~/.cursor/plugins/local/bitsweave
```

Restart Cursor, then confirm the BitsWeave MCP server appears under Customize.

## Layout

```
.cursor-plugin/marketplace.json
plugins/bitsweave/.cursor-plugin/plugin.json
plugins/bitsweave/mcp.json
plugins/bitsweave/assets/logo.svg
LICENSE
README.md
```

## Auth

First MCP tool call starts BitsWeave OAuth. This package ships no tokens.

## Links

- Product: https://bitsweave.com
- Repo: https://github.com/kirchoff-digital/bitsweave-cursor-plugin
- Official submit (later): https://cursor.com/marketplace/publish
