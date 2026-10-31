# Backlog final

Status por inspeção em 31/10/2026. “Concluído no código” não significa demonstrado ou aceito pelo cliente. IDs originais são preservados quando identificados no histórico.

## Concluído no código
| Frente | Entrega | Evidência |
|---|---|---|
| ST-003 / qualidade | Setup, testes com mocks e gates separados | `1c3786df`, `2d8abb82` |
| ST-013 / ST-020 | Primitivos do Design System | `610e9b9d`, ajustes `a94c3c0c` |
| ST-014 / ST-015 | Alterações relativas a slug/publicação e view registradas no histórico | `f6edeacd`, `eeb58da8`; implantação no banco a confirmar |
| ST-016 / ST-023 / ST-024 | Página SSR, Portfólio e Tripulação | `e0974a96`, `29360c47`, `f084bf1f` |
| ST-019 | Publicação e acesso ao link pela tripulação | `512705e5`, `21ea7622`, `c77cf3dc` |
| Página pública | Gestão e propostas; testes de visibilidade, empresa e sitemap | `6290441b`, `c88e5527`, `721b927f`, `cc358971` |
| Orbitinho | Contexto seguro, permissões e navegação | `ead14d45`, `6fb6a505`, `e0336010` |
| EF-G01–G05 / G07–G08 | Arquitetura, conhecimento, comandos, voz, personalidade e testes | `9e7b4f23`, `c21fc862`, `30d7994c`, `0dac88fd`, `f2766653`, `a1a68744`, `0ce6a03d` |
| Orbitinho | Cancelamento, estabilidade de voz e orientação em inglês | `172f3235`, `cf0a6e48` |

## Removido do escopo
- Orbitinho na IDE: retirado conforme registro de atualização do cliente em `SETUP_LOCAL.md`; não apresentar MCP como entrega da IDE.
- Apresentação final (item 5): excluída deste pacote por solicitação do usuário. Isso não constitui dispensa institucional da apresentação.

## Melhorias futuras propostas
- Completar migrations, seeds e testes de policies para recriação segura do ambiente.
- Reduzir dependência de filtros manuais sobre cliente administrativo.
- Ampliar regressão ponta a ponta de áudio e acessibilidade em aparelhos reais.
- Consolidar documentação histórica e matriz de evidências para evitar status contraditórios.

Essas melhorias são recomendações de continuidade, sem compromisso de prazo ou aceite atribuído ao cliente.
