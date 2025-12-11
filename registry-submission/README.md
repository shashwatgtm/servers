# GTM Alpha MCP Server - Registry Submission

This directory contains the registration file for submitting the GTM Alpha MCP Server to the official MCP Registry.

## Server Details

- **Name**: `io.github.shashwatgtm/gtm-alpha-mcp-server`
- **npm Package**: `@shashwatgtmalpha/gtm-alpha-mcp-server@1.0.1`
- **Live Endpoint**: https://gtmalpha.netlify.app/.netlify/functions/mcp
- **Repository**: https://github.com/shashwatgtm/gtm-expert-schema

## EPIC Framework

The GTM Alpha MCP Server provides professional go-to-market consultation using the EPIC framework:

- **E** - Ecosystem & ABM (Account-Based Marketing)
- **P** - Product-Led Growth
- **I** - Inbound & Outbound Demand Generation
- **C** - Community-Led Planning

## Available Tools

| Tool | Description |
|------|-------------|
| `gtm_alpha_real_consultation` | Professional GTM consultation with EPIC framework analysis |
| `epic_progress_tracker` | Track progress across EPIC dimensions with 30-day persistence |
| `epic_framework_deep_audit` | Comprehensive audit of GTM strategy using EPIC framework |
| `premium_consultation_scheduler` | Schedule premium consultation sessions |

## Submission Instructions

To submit this server to the MCP Registry:

1. **Install the MCP Publisher CLI**:
   ```bash
   # Clone and build
   git clone https://github.com/modelcontextprotocol/registry.git
   cd registry
   make publisher
   ```

2. **Authenticate with GitHub**:
   ```bash
   mcp-publisher login github
   ```

3. **Ensure your npm package has the `mcpName` field**:
   Add to your package.json:
   ```json
   {
     "mcpName": "io.github.shashwatgtm/gtm-alpha-mcp-server"
   }
   ```

4. **Publish to the registry**:
   ```bash
   mcp-publisher publish
   ```

5. **Verify submission**:
   ```bash
   curl "https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.shashwatgtm/gtm-alpha-mcp-server"
   ```

## Usage

### Via npm (stdio transport)
```json
{
  "mcpServers": {
    "gtm-alpha": {
      "command": "npx",
      "args": ["@shashwatgtmalpha/gtm-alpha-mcp-server"]
    }
  }
}
```

### Via Remote Endpoint (SSE transport)
```json
{
  "mcpServers": {
    "gtm-alpha": {
      "url": "https://gtmalpha.netlify.app/.netlify/functions/mcp",
      "transport": "sse"
    }
  }
}
```

## Registry Links

- MCP Registry: https://github.com/modelcontextprotocol/registry
- Registry UI: https://registry.modelcontextprotocol.io/
- Quickstart Guide: https://github.com/modelcontextprotocol/registry/blob/main/docs/modelcontextprotocol-io/quickstart.mdx
