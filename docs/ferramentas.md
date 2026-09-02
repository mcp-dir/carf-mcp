# Ferramentas

CARF (Recursos Fiscais) expõe 4 ferramentas (todas somente leitura).

### 1. `jurisprudencia_buscar`
**Input**: `termo`, `tipo` (opcional), `tribunais` (opcional), `data_de` (opcional), `data_ate` (opcional), `ordenar` (opcional), `max` (opcional)

Busca jurisprudência (acórdãos, súmulas, orientações jurisprudenciais, temas) por termo ou tese.

### 2. `jurisprudencia_sumulas`
**Input**: `termo`, `max` (opcional)

Busca SÚMULAS (incluindo vinculantes) por termo.

### 3. `jurisprudencia_documento`
**Input**: `id` (opcional), `numeracao` (opcional), `tribunal` (opcional), `ids` (opcional)

Lê o INTEIRO TEOR de uma decisão (texto completo do acórdão, não o resumo).

### 4. `carf_consultar`
**Input**: `CPF`, `CNPJ`, `completo` (opcional)

Consulta processos de uma pessoa ou empresa no Conselho Administrativo de Recursos Fiscais (CARF) a partir do CPF ou CNPJ.

## Prompts de exemplo

```
Acórdãos do CARF sobre ágio interno em reorganização societária
O que o CARF decide sobre glosa de despesa com royalties?
O Judiciário confirma o entendimento do CARF sobre PIS e COFINS na importação?
O CNPJ 12345678000190 tem processo no CARF?
Leia o inteiro teor do acórdão que você achou e resuma a tese
```
