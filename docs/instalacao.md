# Instalação detalhada

SENATRAN: Meus Veículos - Possuidor (Detalhes) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_senatran_meus_veiculos_info`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_senatran_meus_veiculos_info` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_senatran_meus_veiculos_info` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_senatran_meus_veiculos_info` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.senatran_meus_veiculos_info` (ou `servers.senatran_meus_veiculos_info` no VS Code) do config do cliente e reinicie.
