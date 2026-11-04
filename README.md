# FragAI System MCP Catalogue

Built-in system MCP filter definitions for the FragAI Governance Platform. This is separate from the remote MCP server catalogue.

The initial entry is `pii-filter.yaml`. It uses the `filter_pii` tool at `/mcp` on port 8080 and references the planned image `ghcr.io/harshdeshmukh26/fragai-pii-filter:0.1.0`.

**Do not connect this catalogue to a production installation until the image has been built, tested, published, and made pullable by the installation.** The filter source currently lives in [yugantb24/FragAI-MCP-filters-](https://github.com/yugantb24/FragAI-MCP-filters-).

Validate this catalogue from the Governance Platform repository:

```powershell
go run . mcp validate-system-catalog-yaml "C:\Users\deshm\Documents\Codex\2026-09-01\iw\FragAI-System-MCP-Catalogue"
```

Catalogue entries only make filters available in the picker. An administrator must create a filter, attach it to selected MCP traffic, and verify the gateway and audit behavior before relying on it.
