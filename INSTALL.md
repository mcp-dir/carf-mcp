# Instalação rápida

CARF (Recursos Fiscais) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_carf`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

Este MCP é **grátis e sem login** pra uso básico — funciona assim que você instala. (Login opcional via `app.mcp.ai` só dá limites maiores / histórico.)

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `CARF (Recursos Fiscais)` / `https://api.mcp.ai/p_carf`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "carf": { "type": "http", "url": "https://api.mcp.ai/p_carf" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=carf&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jYXJmIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "carf": { "url": "https://api.mcp.ai/p_carf" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=carf&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_carf%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "carf": { "type": "http", "url": "https://api.mcp.ai/p_carf" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_carf
```

Dúvidas? [carf@mcp.ai](mailto:carf@mcp.ai)
