---
name: senatran_meus_veiculos_info-mcp
description: Skill da REST API do SENATRAN: Meus Veículos - Possuidor (Detalhes) na MCP.AI: 1 endpoint em /api/senatran_meus_veiculos_info. SENATRAN: Meus Veículos - Possuidor (Detalhes), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# SENATRAN: Meus Veículos - Possuidor (Detalhes) — REST API skill

Você tem acesso à **SENATRAN: Meus Veículos - Possuidor (Detalhes)** REST API na MCP.AI.

> SENATRAN: Meus Veículos - Possuidor (Detalhes), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/senatran_meus_veiculos_info
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
curl -X POST https://api.mcp.ai/api/senatran_meus_veiculos_info/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"login_cpf":"...","login_senha":"...","placa":"...","renavam":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/senatran_meus_veiculos_info/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `senatran_meus_veiculos_info_consultar`

SENATRAN: Meus Veículos - Possuidor (Detalhes), consulta em fonte oficial. _(POST /api/senatran_meus_veiculos_info/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `login_cpf` | string | Sim | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `placa` | string | Sim | Parâmetro de consulta "placa". |
| `renavam` | string | Sim | Parâmetro de consulta "renavam". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_senatran_meus_veiculos_info` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
