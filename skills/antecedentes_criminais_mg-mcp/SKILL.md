---
name: antecedentes_criminais_mg-mcp
description: Skill da REST API do Antecedentes Criminais: MG na MCP.AI: 1 endpoint em /api/antecedentes_criminais_mg. Antecedentes Criminais: MG, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Antecedentes Criminais: MG — REST API skill

Você tem acesso à **Antecedentes Criminais: MG** REST API na MCP.AI.

> Antecedentes Criminais: MG, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/antecedentes_criminais_mg
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
curl -X POST https://api.mcp.ai/api/antecedentes_criminais_mg/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/antecedentes_criminais_mg/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `antecedentes_criminais_mg_consultar`

Antecedentes Criminais: MG, consulta em fonte oficial. _(POST /api/antecedentes_criminais_mg/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `rg` | string | Não | Parâmetro de consulta "rg". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_antecedentes_criminais_mg` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
