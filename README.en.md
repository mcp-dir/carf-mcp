# CARF (Recursos Fiscais)

### CARF for Claude, Cursor and AI agents: rulings by thesis and proceedings by taxpayer

Two **CARF** lookups on a single connection: search rulings and binding summaries by term or thesis for free, and look up a taxpayer's proceedings by CPF or CNPJ when you need them. The case law search also reaches 16 other Brazilian courts. Hosted by the platform, no login.

- 📚 **CARF rulings and binding summaries by thesis**, free
- 🔎 **A taxpayer's proceedings** by CPF or CNPJ, when you need the concrete case
- ⚖️ **16 more courts on the same connection**, to check how the Judiciary treated the same thesis
- ⚠️ **Flags what does not bind a judge**: CARF rulings bind the tax authority, and every result says so
- 🎯 **The snippet that actually MATCHED**, not the boilerplate opening
- 🔗 **Link to the official source** on every result
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue

[Versão em português](README.md) · [Full docs (PT-BR)](docs/) · [Agent skill](skills/)

---

## One-click install

### Claude (Web and Desktop)

Anthropic unified MCP installation at `claude.ai/customize/connectors`. **The same link works for Claude Web and Claude Desktop** (just be logged in):

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (if the deeplink does not open): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → paste **Name** `CARF (Recursos Fiscais)` and **URL** `https://api.mcp.ai/p_carf`.

### Cursor

[➕ Install CARF (Recursos Fiscais) in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=carf&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jYXJmIn0=)

### VS Code (Copilot Chat)

[➕ Install CARF (Recursos Fiscais) in VS Code](vscode:mcp/install?name=carf&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_carf%22%7D)

### ChatGPT, Manus, OpenClaw and 40+ other clients

Works with any MCP client that speaks **MCP over HTTP**. The server URL is always:

```
https://api.mcp.ai/p_carf
```

Per-client details: [INSTALL.md](INSTALL.md).

---

## Example prompts

```
CARF rulings on internal goodwill in corporate reorganisation
What does CARF hold on disallowed royalty expenses?
Does the Judiciary confirm CARF's position on PIS and COFINS at import?
Does CNPJ 12345678000190 have a CARF proceeding?
Read the full text of the ruling you found and summarise the holding
```

---

## 4 tools available

| Tool | Description |
|---|---|
| `jurisprudencia_buscar` | Busca jurisprudência (acórdãos, súmulas, orientações jurisprudenciais, temas) por termo ou tese. |
| `jurisprudencia_sumulas` | Busca SÚMULAS (incluindo vinculantes) por termo. |
| `jurisprudencia_documento` | Lê o INTEIRO TEOR de uma decisão (texto completo do acórdão, não o resumo). |
| `carf_consultar` | Consulta processos de uma pessoa ou empresa no Conselho Administrativo de Recursos Fiscais (CARF) a partir do CPF ou CNPJ. |

Details for each tool: [docs/ferramentas.md](docs/ferramentas.md) (PT-BR)

---

## Pricing

Prepaid credit wallet, pay per use. See [docs/precos.md](docs/precos.md) (PT-BR).

---

## Privacy & data protection

- **Read-only**, no tool changes data at the source.
- **Sub-processors**: the LLM host you choose (Claude, ChatGPT, Cursor, your own agent). Full list in [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Data returned by the tools is sent to **the LLM host you choose**, a sub-processor outside our control. We recommend plans with training opt-out.

---

## FAQ

**O que é grátis e o que é pago?**
A busca de acórdãos e súmulas por termo ou tese é grátis e sem login, e vale também para os outros 16 tribunais da mesma conexão. A consulta de processos de um CPF ou CNPJ no conselho é paga por consulta, com crédito pré-pago.

**Decisão do CARF serve como precedente em juízo?**
Não. O CARF é conselho administrativo do Ministério da Fazenda: as decisões dele vinculam a Receita Federal e orientam o contencioso fiscal, mas não vinculam o juiz. Todo resultado vem marcado com essa ressalva, justamente para não ser citado como precedente judicial.

**Dá para comparar o CARF com o Judiciário?**
Sim, e numa pergunta só: a mesma conexão serve STF, STJ, TRF3, TRF4 e os tribunais de justiça estaduais, então dá para pedir a posição administrativa e a judicial lado a lado, cada uma com o link da fonte oficial.

**Precisa de login ou certificado?**
Não. A busca de acórdãos é livre. Para a consulta por CPF ou CNPJ basta ter crédito na carteira do workspace, sem conta em nenhum órgão.

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills, tudo MIT.


---

## Support

- 📧 [carf@mcp.ai](mailto:carf@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/carf-mcp/issues)
- 📄 [docs/](docs/)

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_carf` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
