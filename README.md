# CARF (Recursos Fiscais)

### CARF no Claude, Cursor e agentes de IA: acórdãos por tese e processos por CNPJ

Duas consultas ao **CARF** numa conexão só: busque acórdãos e súmulas por termo ou tese, de graça, e consulte os processos de um CPF ou CNPJ no conselho quando precisar. A busca de acórdãos alcança ainda outros 16 tribunais brasileiros, do STF aos tribunais de justiça estaduais. Hospedado pela plataforma, sem login.

- 📚 **Acórdãos e súmulas do CARF por tese**, de graça
- 🔎 **Processos de um CPF ou CNPJ** no conselho, quando você precisa do caso concreto
- ⚖️ **Mais 16 tribunais na mesma conexão**, do STF aos TJs, pra conferir como o Judiciário tratou a mesma tese
- ⚠️ **Marca o que NÃO vincula juiz**: decisão do CARF vincula a Receita Federal, e todo resultado diz isso
- 🎯 **O trecho que CASOU a busca**, não a abertura burocrática do acórdão
- 🔗 **Link na fonte oficial** em cada resultado, para conferência
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `CARF (Recursos Fiscais)` e **URL** `https://api.mcp.ai/p_carf`.

### Cursor

[➕ Instalar CARF (Recursos Fiscais) no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=carf&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jYXJmIn0=)

### VS Code (Copilot Chat)

[➕ Instalar CARF (Recursos Fiscais) no VS Code](vscode:mcp/install?name=carf&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_carf%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_carf
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Acórdãos do CARF sobre ágio interno em reorganização societária
O que o CARF decide sobre glosa de despesa com royalties?
O Judiciário confirma o entendimento do CARF sobre PIS e COFINS na importação?
O CNPJ 12345678000190 tem processo no CARF?
Leia o inteiro teor do acórdão que você achou e resuma a tese
```

---

## 4 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `jurisprudencia_buscar` | Busca jurisprudência (acórdãos, súmulas, orientações jurisprudenciais, temas) por termo ou tese. |
| `jurisprudencia_sumulas` | Busca SÚMULAS (incluindo vinculantes) por termo. |
| `jurisprudencia_documento` | Lê o INTEIRO TEOR de uma decisão (texto completo do acórdão, não o resumo). |
| `carf_consultar` | Consulta processos de uma pessoa ou empresa no Conselho Administrativo de Recursos Fiscais (CARF) a partir do CPF ou CNPJ. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Pré-pago (carteira de créditos), paga por uso. Veja [docs/precos.md](docs/precos.md).

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

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

## Suporte

- 📧 [carf@mcp.ai](mailto:carf@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/carf-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_carf` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
