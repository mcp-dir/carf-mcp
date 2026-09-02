# Instalação detalhada

CARF (Recursos Fiscais) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_carf`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_carf` | nenhuma (grátis) |
| Cursor | `https://api.mcp.ai/p_carf` | nenhuma |
| VS Code (Copilot) | `https://api.mcp.ai/p_carf` | nenhuma |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.carf` (ou `servers.carf` no VS Code) do config do cliente e reinicie.
