# FragAI System MCP Catalogue

Built-in system MCP filter definitions for the FragAI Governance Platform. This is separate from the remote MCP server catalogue.

The catalogue defines three filters:

| Entry | Filter tool | Container port |
| --- | --- | --- |
| `pii-filter.yaml` | `filter_pii` | 8080 |
| `prompt-injection-filter.yaml` | `filter_prompt_injection` | 8081 |
| `jailbreak-filter.yaml` | `filter_jailbreak` | 8082 |

Each entry points to a versioned image under `ghcr.io/harshdeshmukh26` and exposes `/mcp`.

**Before using an entry, confirm its image has been built, tested, published, and made pullable by the installation.** Review the bundled model terms before distributing the jailbreak image. The filter source currently lives in [yugantb24/FragAI-MCP-filters-](https://github.com/yugantb24/FragAI-MCP-filters-).

Validate this catalogue from the Governance Platform repository:

```powershell
go run . mcp validate-system-catalog-yaml "<path-to-cloned-FragAI-System-MCP-Catalogue>"
```

Catalogue entries only make filters available in the picker. An administrator must create a filter, attach it to selected MCP traffic, and verify the gateway and audit behavior before relying on it.
