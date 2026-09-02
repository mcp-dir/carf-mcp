---
name: carf-mcp
description: CARF (Conselho Administrativo de Recursos Fiscais) para agentes de IA, com DUAS capacidades na mesma conexão: (1) busca GRÁTIS de acórdãos e súmulas por termo ou tese, que alcança também outros 16 tribunais brasileiros (STF, STJ, TST, TRF3, TRF4 e os TJs estaduais); (2) consulta PAGA dos processos de um CPF ou CNPJ no conselho, via carf_consultar. Use a busca quando o usuário perguntar o que o CARF decide sobre uma tese, e a consulta quando ele der um CPF/CNPJ e quiser o caso concreto. SEMPRE avise que decisão do CARF vincula a Receita Federal e NÃO vincula o juiz, e nunca a cite como precedente judicial. Para confrontar administrativo e judicial, restrinja a busca com tribunais:["STJ"] ou similar na mesma conexão. Orquestra jurisprudencia_buscar, jurisprudencia_sumulas, jurisprudencia_documento e carf_consultar em https://api.mcp.ai/p_carf.
---

# CARF (Recursos Fiscais) — REST API skill

Você tem acesso à **CARF (Recursos Fiscais)** REST API na MCP.AI.

> Duas consultas ao **CARF** numa conexão só: busque acórdãos e súmulas por termo ou tese, de graça, e consulte os processos de um CPF ou CNPJ no conselho quando precisar. A busca de acórdãos alcança ainda outros 16 tribunais brasileiros, do STF aos tribunais de justiça estaduais. Hospedado pela plataforma, sem login.

## Base URL

```
https://api.mcp.ai/api/carf
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/carf/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"CPF":"...","CNPJ":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/carf/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `carf_consultar`

Consulta processos de uma pessoa ou empresa no Conselho Administrativo de Recursos Fiscais (CARF) a partir do CPF ou CNPJ. _(POST /api/carf/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CPF` | string | Sim | Parâmetro de consulta "CPF". |
| `CNPJ` | string | Sim | Parâmetro de consulta "CNPJ". |
| `completo` | boolean | Não | Opcional. Por padrão (false) listas longas vêm resumidas aos primeiros itens, com a contagem total preservada. Use true para a resposta COMPLETA na mesma consulta. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_carf` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
