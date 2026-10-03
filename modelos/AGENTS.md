# Instruções do projeto — planejamento e execução por blocos

> Modelo Hubbi para adaptar. Preserve regras existentes e resolva conflitos antes de incorporar. Preencha os campos pendentes.

## Contexto e comunicação

- Idioma: PT-BR. Público e objetivo do projeto: [preencher].
- Explique problemas nesta ordem: português simples, exemplo concreto, consequência, detalhe técnico curto e uma decisão com recomendação.
- Traduza termos técnicos na primeira ocorrência; não alegue resultado sem evidência.

## Planejamento

- Para projeto novo ou demanda com várias etapas, faça inspeção curta, apresente plano e aguarde autorização antes de implementar.
- Ajuste localizado, claro e de baixo risco dispensa plano formal. Se crescer, planeje antes de ampliar.
- Plano deve conter objetivo, partida, entrega demonstrável, escopo/exclusões, mapa completo dos blocos, dependências/autorizações, passos, aceite e verificações por bloco, estimativas, paradas e texto pronto de execução.
- Recomende modelo e esforço disponíveis por bloco, justificando qualidade, velocidade, consumo e quando reavaliar. Não troque silenciosamente nem use Max/Ultra por padrão.
- Defina execução individual ou delegada; prefira individual sem ganho concreto de paralelismo.
- Se delegar: um coordenador e até dois subagentes, com tarefas independentes, entradas, resultado, área isolada, modelo/esforço e parada. Integração e verificação são do coordenador. Expansão/subdelegação exige aprovação explícita.
- Aprovar o plano e autorizar sua execução são decisões distintas; registre a versão autorizada.

## Execução contínua

- A autorização de execução cobre todos os blocos descritos, inclusive os não triviais, sem novo “ok” a cada transição.
- Execute, verifique, registre checkpoint e comece automaticamente o próximo bloco aprovado.
- Checkpoint informa resultado, evidência, limitações relevantes e próximo passo.
- Reaproveite evidências válidas. Repita verificações por mudança relevante, inconclusão ou exigência do projeto.
- Duas tentativas equivalentes sem evidência nova exigem mudança de abordagem.
- Estimativas orientam expectativa; não impõem teto automático nem espera artificial. Limites reais da ferramenta continuam válidos.
- Pare por conclusão, decisão externa indispensável, risco novo relevante, autorização ausente, impedimento real ou ampliação material do escopo.
- Apresente mudanças importantes no plano antes de executar; ajustes rotineiros dentro do resultado aprovado permanecem autorizados.

## Preservação, segurança e publicação

- Sincronize e confira diferenças locais/remotas nas duas direções antes de editar. Use branch de tarefa e worktree isolado; não commite diretamente na principal.
- Nunca descarte, reverta ou sobrescreva trabalho alheio sem autorização explícita. Sinalize problemas de outra frente.
- Não exponha credenciais ou dados pessoais em conteúdo, logs e histórico de versões.
- Autorizações externas/produção: [definir]. Não presuma publicação, envio de mensagens, banco real ou exclusão de dados a partir da autorização local.
- Procedimento de publicação, versão e recuperação: [definir conforme o projeto].
- Se uma correção reduzir números exibidos a clientes, alinhe a mudança antes de publicar.

## Entrega e registros

- Verificações obrigatórias impedidas mantêm o critério incompleto; registre a limitação.
- Distinga verificado localmente, integrado, aguardando publicação e publicado/verificado.
- Demonstre o resultado no ambiente combinado e registre versão/referência quando pertinente.
- Atualize plano e registros de continuidade quando resolver uma pendência, preservando o histórico e acrescentando evidência e estado atual.
- Registro de continuidade do projeto: [caminho]. Registre resultado, mudanças, verificações, pendências e próximos trabalhos fora do escopo.
