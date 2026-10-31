# Backlog final — Startellite

Este backlog consolida as entregas de Wesley Lima Silva, Guilherme Kenzo Taba Nakamura e Pedro Santos (Pedro-7-BFR), agrupadas pelo resultado que oferecem ao produto.

**Base de referência:** código e histórico consultados em 31/10/2026, conforme [Evidências e rastreabilidade](docs/EVIDENCIAS.md). Os IDs `ST-*` e `EF-G*` preservam as referências encontradas no histórico. Os IDs `BF-*` organizam este documento e não representam novos tickets no sistema do cliente.

## Leitura dos status e critérios

- **Implementado:** entrega identificada no código ou no histórico indicado. Não equivale, por si só, a implantação ou aceite do cliente.
- **Removido do escopo:** funcionalidade retirada da entrega do produto.
- **Melhoria futura:** recomendação de continuidade, sem prazo ou responsável contratado.

Os critérios abaixo descrevem o resultado esperado de cada entrega e facilitam sua revisão. Eles não representam novos testes executados ou termos de aceite assinados. A autoria indica os contribuidores dos commits citados, sem atribuir a eles toda a plataforma.

## Entregas implementadas

### Página pública das Espaçonaves

#### ST-014 / ST-015 — Identificação e contrato público

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Registrar slug e estado de publicação e definir a projeção pública dos dados.
- **Critério de conclusão:** Campos de identificação/publicação e view registrados no histórico; leitura pública limitada ao contrato definido.
- **Evidências:** [f6edeacd](https://github.com/HenriqueRBomfim/startellite-frontend/commit/f6edeacd97d44bc172b6ad6924ab43aa3e43c2e2), [eeb58da8](https://github.com/HenriqueRBomfim/startellite-frontend/commit/eeb58da87789d152f03da692800519c63e285faa).

#### ST-016 — Perfil público com SSR e compartilhamento

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Apresentar a equipe em endereço próprio, com apresentação e metadados.
- **Critério de conclusão:** Rota `/spaceships/[slug]`, renderização no servidor, metadados e tratamento de perfil indisponível.
- **Evidências:** [e0974a96](https://github.com/HenriqueRBomfim/startellite-frontend/commit/e0974a960d3bd1706dce406194e3ad115abc9fcd).

#### ST-023 / ST-024 — Portfólio e Tripulação

- **Status:** Implementado.
- **Contribuidores:** Guilherme e Pedro.
- **Entrega:** Organizar projetos e integrantes em abas e distinguir ausência de conteúdo de falha de carregamento.
- **Critério de conclusão:** Abas próprias, estados vazios e tratamento de erro para as duas listas.
- **Evidências:** [29360c47](https://github.com/HenriqueRBomfim/startellite-frontend/commit/29360c47f198a0a15525bf5598296114092143d2), [f084bf1f](https://github.com/HenriqueRBomfim/startellite-frontend/commit/f084bf1fdb89e591e5c4b2e1c6f95dfa8b792996).

#### ST-019 — Publicação e endereço da página

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Permitir alternar a visibilidade e disponibilizar o endereço público para a tripulação.
- **Critério de conclusão:** Controle pública/privada e aba Página com endereço completo acessível aos membros.
- **Evidências:** [512705e5](https://github.com/HenriqueRBomfim/startellite-frontend/commit/512705e51a8b441e0a9d7f163c5714982674332a), [21ea7622](https://github.com/HenriqueRBomfim/startellite-frontend/commit/21ea762255526e6903d213dc709bf146a6441ccb), [c77cf3dc](https://github.com/HenriqueRBomfim/startellite-frontend/commit/c77cf3dc6b5533062a25a74c45068ba35b24b934), [dcef5567](https://github.com/HenriqueRBomfim/startellite-frontend/commit/dcef55672fdaa11bb5473362f065939ef1c36f23).

#### BF-01 — Gestão e propostas na página pública

- **Status:** Implementado.
- **Contribuidores:** Wesley e Pedro.
- **Entrega:** Conectar a apresentação da Espaçonave à gestão e ao fluxo de propostas com autorização.
- **Critério de conclusão:** Implementação da gestão e propostas acompanhada de testes de permissões de empresa.
- **Evidências:** [6290441b](https://github.com/HenriqueRBomfim/startellite-frontend/commit/6290441b815a6e4893555e700b7421bb51e87718), [721b927f](https://github.com/HenriqueRBomfim/startellite-frontend/commit/721b927f591b087de0c8ceeebe419874334dc6ad).

#### BF-02 — Visibilidade e indexação pública

- **Status:** Implementado.
- **Contribuidores:** Pedro e Wesley.
- **Entrega:** Proteger a publicação e cobrir a consulta pública usada pelo sitemap.
- **Critério de conclusão:** Testes de visibilidade, acesso público e consulta do sitemap presentes no histórico.
- **Evidências:** [c88e5527](https://github.com/HenriqueRBomfim/startellite-frontend/commit/c88e5527e6eb2ddcb6659b41359d4b659fb75ad5), [cc358971](https://github.com/HenriqueRBomfim/startellite-frontend/commit/cc3589715f7559ab736bddbb06fe220f60333085), [85882185](https://github.com/HenriqueRBomfim/startellite-frontend/commit/858821851e98d6a35f10b2b6731091832171871e).


### Design System e consistência da interface

#### ST-013 / ST-020 — Componentes e tokens reutilizáveis

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Padronizar componentes para facilitar consistência visual e manutenção.
- **Critério de conclusão:** Inventário e implementação de primitivos do Design System registrados.
- **Evidências:** [c35889a4](https://github.com/HenriqueRBomfim/startellite-frontend/commit/c35889a4f2e6898d1d7d683ce171f1fb581ede13), [610e9b9d](https://github.com/HenriqueRBomfim/startellite-frontend/commit/610e9b9d97dfc6b6c0a104109fcbf0de417beb5d).

#### BF-03 — Abas e demonstração do Design System

- **Status:** Implementado.
- **Contribuidores:** Pedro.
- **Entrega:** Refinar a navegação por abas e a apresentação dos componentes.
- **Critério de conclusão:** Ajustes de interface e da demonstração registrados no commit.
- **Evidências:** [a94c3c0c](https://github.com/HenriqueRBomfim/startellite-frontend/commit/a94c3c0c4ec88b7ce73641772426d57f3ef222a5).


### Orbitinho: orientação, navegação e ações

#### EF-G01 / EF-G02 — Arquitetura e base de conhecimento

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Mapear componentes, intenções e rotas e estruturar respostas sobre a plataforma.
- **Critério de conclusão:** Arquitetura documentada, base de conhecimento e conjunto de avaliação versionados.
- **Evidências:** [9e7b4f23](https://github.com/HenriqueRBomfim/startellite-frontend/commit/9e7b4f234f705820347d65ddc8685ee7b67ab000), [c21fc862](https://github.com/HenriqueRBomfim/startellite-frontend/commit/c21fc8628956bb6a9634e34f3554fdc48d238ef7), [4856b66f](https://github.com/HenriqueRBomfim/startellite-frontend/commit/4856b66fccb9c69e2f2357b48eaed70ae0e3386b).

#### EF-G03 / BF-04 — Navegação conforme o perfil

- **Status:** Implementado.
- **Contribuidores:** Guilherme e Wesley.
- **Entrega:** Interpretar destinos, separar contextos de empresa/satélite e esclarecer pedidos ambíguos.
- **Critério de conclusão:** Comandos por contexto, aliases centralizados e pedido de esclarecimento para destino ambíguo.
- **Evidências:** [30d7994c](https://github.com/HenriqueRBomfim/startellite-frontend/commit/30d7994ca28b9bffe7baa49e90d37c3a430a0909), [c1774b85](https://github.com/HenriqueRBomfim/startellite-frontend/commit/c1774b85081db941ced261058ec81941aad1b357), [562d89bc](https://github.com/HenriqueRBomfim/startellite-frontend/commit/562d89bce01fd69679cd99ef43e8e2c362ce05fa), [a992822c](https://github.com/HenriqueRBomfim/startellite-frontend/commit/a992822c4e8f5032fbf4813ecdecc87308f9c888).

#### BF-05 — Contexto e autorização no servidor

- **Status:** Implementado.
- **Contribuidores:** Wesley.
- **Entrega:** Restringir projetos e tarefas consultados à identidade e aos acessos do usuário.
- **Critério de conclusão:** Verificação de acesso no contexto e correções de segurança na execução dos comandos.
- **Evidências:** [ead14d45](https://github.com/HenriqueRBomfim/startellite-frontend/commit/ead14d458721d187dc1cf0584b0c65e435218632), [a37b63b9](https://github.com/HenriqueRBomfim/startellite-frontend/commit/a37b63b998aceb0c3422ffd545e7014de2c26391), [6fb6a505](https://github.com/HenriqueRBomfim/startellite-frontend/commit/6fb6a50595e08944835054fb218eee5bebe7f26c), [e0336010](https://github.com/HenriqueRBomfim/startellite-frontend/commit/e0336010ecd6e7479d4106b9f915726e0d2d0b2e).

#### EF-G03 / BF-06 — Confirmação e cancelamento

- **Status:** Implementado.
- **Contribuidores:** Guilherme e Wesley.
- **Entrega:** Controlar a execução das ações e manter tratamento seguro no fallback.
- **Critério de conclusão:** Confirmação, cancelamento e consulta de tarefas tratados no fluxo e em testes.
- **Evidências:** [a7ffebc1](https://github.com/HenriqueRBomfim/startellite-frontend/commit/a7ffebc17f0f403f6a8f126a0c72d61a2f995b70), [6fb6a505](https://github.com/HenriqueRBomfim/startellite-frontend/commit/6fb6a50595e08944835054fb218eee5bebe7f26c).

#### EF-G04 — Entrada por voz e recuperação de falhas

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Oferecer comandos por voz com feedback e tratamento de falhas de transcrição.
- **Critério de conclusão:** Fluxo de áudio, catálogo de comandos e retentativa de transcrição implementados.
- **Evidências:** [0dac88fd](https://github.com/HenriqueRBomfim/startellite-frontend/commit/0dac88fd78f56c4792590493f9e47ee1daf40cc8), [6af8b298](https://github.com/HenriqueRBomfim/startellite-frontend/commit/6af8b2989a8aee5eb287e8399fab206aea4a23c9).

#### EF-G05 — Hands-free, personalidade e acessibilidade

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Melhorar a interação contínua e dar controle sobre a reprodução das respostas.
- **Critério de conclusão:** Modo hands-free, ajustes de personalidade/acessibilidade e botão de ativação da voz.
- **Evidências:** [f2766653](https://github.com/HenriqueRBomfim/startellite-frontend/commit/f27666535b4280b44ea58af417ba7a69670169f4), [ac97f773](https://github.com/HenriqueRBomfim/startellite-frontend/commit/ac97f77320f84674317d8c97f1547b1f3f8f65df).

#### BF-07 — Estabilidade e apresentação do modal

- **Status:** Implementado.
- **Contribuidores:** Wesley.
- **Entrega:** Reduzir travamentos e ajustar a janela do assistente para diferentes usos.
- **Critério de conclusão:** Modal compacto/personalizável, correções de espera e voz desktop e ampliação de respostas em inglês.
- **Evidências:** [6091daf6](https://github.com/HenriqueRBomfim/startellite-frontend/commit/6091daf6fd83405000b5e76c05f11f9ceae24598), [172f3235](https://github.com/HenriqueRBomfim/startellite-frontend/commit/172f3235e2ad7643ac141893009571bf8f1a06cd), [cf0a6e48](https://github.com/HenriqueRBomfim/startellite-frontend/commit/cf0a6e4800520ec08191b603c45bc0ba8bde9e6e), [22d26af9](https://github.com/HenriqueRBomfim/startellite-frontend/commit/22d26af9989ce56a581a26ca8107252ba97462cb).

#### EF-G07 / EF-G08 — Regressão e evidências do assistente

- **Status:** Implementado.
- **Contribuidores:** Guilherme.
- **Entrega:** Organizar cenários de teste e registrar as correções da frente Orbitinho.
- **Critério de conclusão:** Matriz de testes e documentação de evidências versionadas com ajustes de CI.
- **Evidências:** [a1a68744](https://github.com/HenriqueRBomfim/startellite-frontend/commit/a1a6874444fb8d4de1d70a6fbccf24920aace2a1), [0ce6a03d](https://github.com/HenriqueRBomfim/startellite-frontend/commit/0ce6a03ded885989f914b8881334a5dcee32db81).


### Ambiente, testes e integração contínua

#### ST-003 — Guia de configuração local

- **Status:** Implementado.
- **Contribuidores:** Wesley.
- **Entrega:** Orientar a instalação e a configuração do ambiente de desenvolvimento.
- **Critério de conclusão:** Setup documentado com comandos e cuidados para credenciais.
- **Evidências:** [1c3786df](https://github.com/HenriqueRBomfim/startellite-frontend/commit/1c3786df127446cf990b2a91618ebc9165f57f8d).

#### BF-08 — Testes isolados e verificações de qualidade

- **Status:** Implementado.
- **Contribuidores:** Wesley.
- **Entrega:** Automatizar a detecção de regressões com mocks e checks separados.
- **Critério de conclusão:** Infraestrutura de testes com mocks, lint/typecheck e correções dos bloqueios do quality gate.
- **Evidências:** [2d8abb82](https://github.com/HenriqueRBomfim/startellite-frontend/commit/2d8abb8232a124989b0da2f90884fa8248269045), [f937e48d](https://github.com/HenriqueRBomfim/startellite-frontend/commit/f937e48de46ae6cd7112a9b28639639282d7c48a), [d6ed0fc4](https://github.com/HenriqueRBomfim/startellite-frontend/commit/d6ed0fc4d8266ca808edf12a35ffc1ce8a78078e).

#### BF-09 — Configuração do deploy automatizado

- **Status:** Implementado.
- **Contribuidores:** Wesley.
- **Entrega:** Ajustar o comando de publicação e a vinculação ao projeto Vercel.
- **Critério de conclusão:** Correções de comando e identificação do projeto registradas no histórico.
- **Evidências:** [5d91d521](https://github.com/HenriqueRBomfim/startellite-frontend/commit/5d91d521867529d5987e8fdfef353c63fb0c9f91), [61f9043a](https://github.com/HenriqueRBomfim/startellite-frontend/commit/61f9043a1e74c610ed7a392b60819ed9d8675982), [17c5b32a](https://github.com/HenriqueRBomfim/startellite-frontend/commit/17c5b32a9f6cd743e8bccbe436cff01a92c39566).

## Removido do escopo do produto

| Item | Decisão registrada | Impacto no backlog |
|---|---|---|
| Orbitinho na IDE | Retirado conforme atualização do cliente registrada em `SETUP_LOCAL.md` da origem. | Não compõe as funcionalidades desta entrega; MCP não é apresentado como entrega de integração com IDE. |

## Melhorias futuras propostas

As prioridades organizam uma sequência recomendada para a equipe de continuidade; não constituem compromisso de implementação.

| ID | Prioridade sugerida | Melhoria e benefício | Critério de conclusão | Dependência |
|---|---|---|---|---|
| MF-01 | Alta | Consolidar migrations e dados fictícios de exemplo para tornar o ambiente reproduzível. | Recriar um ambiente de homologação a partir de instruções versionadas, sem copiar dados pessoais de produção. | Schema autorizado e revisão do responsável Supabase. |
| MF-02 | Alta | Ampliar proteção e testes de acesso no banco, reduzindo dependência de filtros manuais administrativos. | Testes com usuários de perfis distintos cobrindo acesso permitido e negado, com policies revisadas. | MF-01 e definição das regras de acesso. |
| MF-03 | Média | Ampliar regressão ponta a ponta de voz em navegadores e aparelhos reais. | Matriz reproduzível cobrindo autorização de microfone, áudio vazio, interrupção, confirmação e alternativa escrita. | Ambiente de homologação, contas de teste e serviços de áudio configurados. |
| MF-04 | Média | Ampliar avaliação de acessibilidade do assistente e dos componentes. | Registrar cenários de teclado, foco, leitor de tela e diferentes tamanhos de tela, com resultados por cenário. | Catálogo de componentes e fluxos de interação. |
| MF-05 | Média | Consolidar registros técnicos e evidências por versão. | Manter uma referência por funcionalidade com commit, ambiente e cenário de verificação, identificando documentos históricos. | Revisão dos documentos da origem e deste pacote. |

## Continuidade e rastreabilidade

Para evoluir um item, preservar seu identificador e vincular a alteração ao commit ou PR correspondente. As melhorias futuras devem receber responsável e estimativa quando forem incorporadas ao planejamento da equipe.

Detalhes de execução e serviços estão no [README](README.md) e no [HANDOFF](HANDOFF.md); arquitetura e contratos estão na [documentação técnica](docs/DOCUMENTACAO_TECNICA.md).
