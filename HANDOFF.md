# Handoff do projeto

## O que não funciona sem configuração
- IA e transcrição não têm funcionamento completo sem Gemini e cota disponível.
- TTS Google depende de identidade federada e configuração do ambiente; a alternativa nativa depende do navegador. Texto permanece como alternativa.
- Uma instalação nova não recria todo o banco somente pelas migrations existentes.
- A página pública depende de uma view e policies corretas. Ausência ou erro pode aparecer como 404; isso não prova que a Espaçonave é privada.

## Bugs e riscos conhecidos
Não foi reproduzido bug funcional nesta sessão, pois a aplicação não foi executada. O documento histórico `docs/orbitinho-evidencias.md` registra isolamento dependente de filtros administrativos, MCP stdio com service role sem autenticação e rotas de áudio sem cota/rate limit. A leitura atual das rotas de áudio confirma exigência de sessão; a resolução completa dos demais riscos exige auditoria no commit e no ambiente implantado. MCP/IDE está fora do escopo e não deve ser exposto com dados reais.

Os registros antigos divergem sobre audit/lint e sobre a disponibilidade da view. Não assumir os números antigos como diagnóstico atual. Safari/iOS, Firefox, autoplay e leitores de tela têm validações manuais pendentes nos documentos da origem.

## Pendências
1. Obter schema estrutural autorizado, revisar view pública, Storage, RLS e consentimentos com o responsável do banco.
2. Rodar instalação, lint, typecheck, testes, build e audit; anexar resultados e SHA.
3. Homologar página pública/privada, propostas e isolamento entre duas contas distintas.
4. Testar microfone autorizado/negado, áudio vazio, indisponibilidade de IA, cancelamento e confirmação sem duplicação.
5. Gravar e anexar o vídeo de 1–3 minutos; registrar banca e aceite do cliente.

## Acessos e serviços
| Serviço | Acesso necessário | Como transferir |
|---|---|---|
| GitHub origem | Permissão de leitura e, para manutenção, PR | Convite da organização/responsável |
| GitHub desta entrega | Manutenção da documentação | Proprietário VTBVN |
| Supabase | Projeto Stage, schema, Auth, Storage e policies | Convite individual, menor privilégio |
| Vercel | Sandbox e produção, variáveis e logs | Convite ao projeto correto |
| Gemini / Google Cloud | Cotas, projeto, identidade TTS | IAM e configuração privada |
| Resend, Stripe, Asaas e Focus NFe | Somente se houver continuidade dos módulos correspondentes | Responsável do cliente; testar em sandbox |

Não há senhas, tokens ou credenciais neste documento. Titulares operacionais, permissões concedidas e URLs privadas de sandbox precisam ser registrados em canal restrito pelo cliente; não foram confirmados nesta entrega.

## Orientações para continuidade
Começar pelo README e snapshot de evidências. Criar branch no código de origem, configurar Stage e validar o banco antes de testar dados reais. Corrigir bloqueios de segurança e configuração antes de promover; só depois realizar a matriz manual e gravar. Promover o commit validado pelos workflows da origem e manter a versão anterior identificada para eventual reversão de deploy; mudanças de banco exigem plano próprio e não devem ser revertidas cegamente.

Para atualizar a entrega, registrar: data, SHA, ambiente, cenários executados, resultado, responsável e link da evidência. A equipe seguinte deve conseguir distinguir código presente, teste automatizado, demonstração e aceite.
