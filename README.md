# Entrega Final Startellite

Entrega de encerramento do Insper Code: produto, documentação e legado. A apresentação final (item 5) foi excluída por solicitação. Este repositório reúne documentação; o código executável permanece no [repositório de origem](https://github.com/HenriqueRBomfim/startellite-frontend).

## Contexto e solução
A Startellite conecta empresas e profissionais e organiza trabalho em projetos, quadros e Espaçonaves (equipes). A entrega acadêmica concentra-se em tornar equipes apresentáveis publicamente, padronizar a interface e facilitar o uso da plataforma pelo Orbitinho, assistente de texto e voz.

## Funcionalidades da entrega
- Página pública `/spaceships/[slug]`, renderizada no servidor, com apresentação, Portfólio, Tripulação e metadados de compartilhamento.
- Gestão da publicação e link público da Espaçonave; tratamento de estados vazios e de erro, e propostas com checagem de acesso de empresa.
- Orbitinho: dúvidas sobre a plataforma, navegação contextual, consulta das próprias tarefas e ações com confirmação, entrada por texto/voz e alternativa escrita em falhas de áudio.
- Design System com tokens e componentes reutilizáveis; testes com mocks e verificações automatizadas.

Implementação identificada no código não equivale a homologação no ambiente do cliente. Consulte as [evidências](docs/EVIDENCIAS.md) e o [handoff](HANDOFF.md).

## Tecnologias e arquitetura geral
Next.js 15.5.x (manifesto: `^15.5.28`), React 19, TypeScript 5.8.x, Tailwind CSS 4, Supabase/PostgreSQL e Auth, Gemini, Google Cloud TTS, Jest e GitHub Actions. A hospedagem configurada é Vercel. A aplicação também integra serviços financeiros e de e-mail preexistentes, fora da autoria atribuída a esta entrega.

Navegador → aplicação Next.js (páginas, API Routes e Server Actions) → Supabase; o servidor integra IA e áudio. O modelo interpreta comandos; a aplicação valida acesso e executa ações. Diagramas e contratos estão na [documentação técnica](docs/DOCUMENTACAO_TECNICA.md).

## Pré-requisitos
Git, Node.js 20 (versão usada pelos workflows; compatibilidade completa da árvore deve ser conferida na instalação), npm e acesso autorizado ao Supabase de homologação. Microfone e contexto seguro HTTPS são necessários para voz; Gemini e TTS exigem configuração adicional. Não existe neste pacote um banco local completo pronto para recriação.

## Instalação e configuração
Execute no código de origem, e não neste repositório documental:

```bash
git clone https://github.com/HenriqueRBomfim/startellite-frontend.git
cd startellite-frontend
git checkout 21880140d80a34b748668c56ed11b57bbe614167
npm ci
cp .env.example .env.local
```

Preencha `.env.local` com credenciais de homologação fornecidas pelo responsável. O checkout fixa a versão analisada; para continuar o desenvolvimento, crie uma branch a partir dela.

## Variáveis de ambiente
| Grupo | Variáveis | Uso |
|---|---|---|
| Supabase público | `NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Cliente e leitura pública |
| Supabase servidor | `SUPABASE_URL`, `SUPABASE_ANON_KEY`, `SUPABASE_SERVICE_ROLE_KEY` | Operações de servidor; service role é secreta |
| IA | `GEMINI_API_KEY`, `GEMINI_TRANSCRIPTION_MODEL` (opcional) | Interpretação e transcrição |
| TTS | `GCP_PROJECT_ID`, `GCP_PROJECT_NUMBER`, `GCP_SERVICE_ACCOUNT_EMAIL`, `GCP_WORKLOAD_IDENTITY_POOL_ID`, `GCP_WORKLOAD_IDENTITY_POOL_PROVIDER_ID`, `VERCEL_TEAM_SLUG` | Identidade federada/OIDC do Google Cloud |
| Aplicação | `NEXT_PUBLIC_APP_URL` | URL do ambiente |
| Outros módulos | Stripe, Asaas, Resend, Focus NFe, VAPID e segredos de cron/webhook | Consultar `.env.example` da origem conforme o fluxo habilitado |

Nenhum valor real está incluído. Nunca prefixar segredo com `NEXT_PUBLIC_`. A chave anônima depende das permissões do banco; não substitui revisão das policies. `.env.local` deve permanecer fora do Git.

## Como executar localmente
```bash
npm run dev
```
O script usa `next dev --turbopack --experimental-https`: confira a URL impressa pelo Next (normalmente `https://localhost:3000`). Certificado e permissões locais podem exigir configuração. Para testes e build:

```bash
npm run lint
npm run typecheck
npm test -- --ci
npm run build
npm start
```

`npm start` exige build anterior. Os testes usam mocks; não comprovam acesso real aos serviços. Para a página fictícia em desenvolvimento, `PUBLIC_SPACESHIP_MOCK=1` habilita dados de demonstração; essa opção é ignorada em produção.

## Estrutura dos repositórios
| Neste repositório | Conteúdo |
|---|---|
| `README.md` | Entrada, instalação e configuração |
| `docs/DOCUMENTACAO_TECNICA.md` | Arquitetura, contratos, dados, segurança, testes e CI/CD |
| `BACKLOG_FINAL.md` | Concluído, pendente, removido e melhorias futuras |
| `HANDOFF.md` | Limitações, acessos e continuidade |
| `docs/VIDEO_DEMONSTRACAO.md` | Roteiro e pendência do vídeo obrigatório |
| `docs/EVIDENCIAS.md` | Snapshot e contribuições rastreáveis |
| `docs/CHECKLIST_ENTREGA.md` | Cobertura dos requisitos e banca |

Na origem: `src/app` contém rotas e Server Actions; `src/components` a interface; `src/context` e `src/hooks` a orquestração do Orbitinho; `src/lib` contratos e regras; `tests` infraestrutura de testes; `supabase` SQL; `.github/workflows` CI/CD.

## Deploy e acesso
Endereço mencionado pelo projeto: https://startellite.com (disponibilidade e versão em produção não verificadas nesta entrega). As configurações de origem distinguem `main`/produção e `stage`/sandbox na Vercel. Este repositório documental não faz deploy da aplicação.

## Autores e atribuição
Wesley Lima Silva; Guilherme Kenzo Taba Nakamura (também Guilherme Taba no Git); Pedro Santos (identificado pelo usuário como Pedro-7-BFR). As contribuições foram extraídas do histórico; a associação do login de Pedro foi fornecida pelo solicitante. HenriqueRBomfim e demais colaboradores são autores da plataforma de origem; não se atribui toda a plataforma aos três integrantes.

Base: branch `main`, commit `21880140d80a34b748668c56ed11b57bbe614167`, consultado em 31/10/2026. Documentação produzida com auxílio de IA e conferida por leitura do código e histórico, sem execução funcional nem aceite do cliente nesta sessão.
