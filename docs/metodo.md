# O método: do pedido à entrega comprovada

[Voltar ao início](../README.md)

## 1. Comece pelo resultado

Uma ideia vaga deixa muitas decisões abertas. “Faça um aplicativo de estudos” pode virar algo maior do que você precisa, consumindo tempo em cadastro de usuário, calendário e recursos que nem foram pedidos.

Um pedido mais útil é: “Quero adicionar 3 tarefas de estudo, concluir 1 e ver essa conclusão preservada quando recarregar a página”. Agora você consegue conferir o resultado e o agente consegue propor um caminho delimitado. Os números são de um exemplo fictício.

Descreva:

- Quem usa e qual problema precisa resolver.
- O que deve passar a ser possível.
- O que existe hoje e pode ser reaproveitado.
- Uma demonstração concreta do sucesso.
- Limites: o que fica fora e quais ações precisam de autorização.

Você não precisa conhecer a solução técnica para fazer esse pedido. O agente deve explicar as escolhas na medida necessária para você decidir.

## 2. Saiba quando planejar

| Situação | Como conduzir |
|---|---|
| Ajuste localizado, claro e de baixo risco | Explicar, executar quando autorizado e conferir, sem plano formal |
| Projeto novo ou demanda com várias etapas | Inspeção curta, plano completo e autorização antes da implementação |
| Integração, regra de negócio, várias áreas ou investigação incerta | Plano com dependências, verificações e decisões explícitas |
| Ajuste simples que cresceu | Parar antes da expansão, apresentar o novo escopo e alinhar o plano |

Trocar o texto de um botão costuma ser um ajuste simples. Fazer esse botão cobrar um pagamento envolve outras etapas e riscos: merece planejamento.

A inspeção inicial serve para descobrir o suficiente para planejar. Use registros e evidências existentes; aprofunde somente as dúvidas que mudam o resultado, o risco ou o caminho.

## 3. Monte dois níveis de plano

**Mapa geral:** apresenta todos os blocos, da partida à entrega. Mostra o que cada um produz, suas dependências e a ordem.

**Detalhe executável:** explica como realizar e conferir cada bloco. Precisa ser suficiente para uma autorização única, sem tentar prever cada linha de código.

O [modelo de plano](../modelos/plano.md) reúne os campos para os dois níveis.

Todo plano com várias etapas deve informar:

1. Objetivo e valor para quem usa.
2. Estado de partida, evidências reaproveitadas e lacunas.
3. Entrega final demonstrável.
4. Escopo que entra e exclusões.
5. Mapa completo dos blocos, com resultado e dependências.
6. Passos e critérios de aceite de cada bloco.
7. Verificações proporcionais ao risco, com ambiente e evidência esperada.
8. Modelo, esforço de raciocínio e decisão sobre subagentes.
9. Acessos e autorizações necessários, incluindo publicação quando pertinente.
10. Estimativa por bloco e total, critérios de parada e texto pronto para execução.

“Critério de aceite” significa a condição que você consegue conferir para aceitar a entrega: funciona como a lista de conferência de uma encomenda.

## 4. Divida por resultado

Um bloco precisa terminar com algo observável. “Mexer na interface” é vago. “Permitir adicionar e visualizar uma tarefa” dá um resultado claro.

Prefira blocos que percorram um pequeno fluxo utilizável. Quando for necessário um bloco de diagnóstico ou preparação, identifique-o e explique o que ele destrava.

| Bloco | Exemplo fictício de resultado | Como conferir |
|---|---|---|
| B01 — adicionar e listar | A lista passa de 0 para 3 tarefas | Adicionar 3 títulos e conferir a contagem |
| B02 — concluir e preservar | 1 das 3 tarefas fica concluída e permanece assim ao recarregar | Marcar, recarregar e conferir títulos e estado |
| B03 — fechar o fluxo | A entrega funciona integrada e tem instruções de uso | Repetir o percurso completo e registrar o ambiente |

Se B02 precisa do resultado de B01, mantenha essa ordem. A existência de vários blocos, por si só, não justifica executar em paralelo.

## 5. Revise e autorize a execução

Antes de autorizar, confira se o resultado corresponde à sua intenção, se o escopo cabe no que deseja fazer e se as verificações realmente mostram sucesso.

Há duas decisões distintas:

- **Aprovar o plano:** o caminho está alinhado.
- **Autorizar a execução:** o agente pode começar e percorrer os blocos descritos.

Você pode resolver ambas em uma mensagem: “Aprovo este plano e autorizo executar B01 a B03”. Se quiser apenas revisar, diga “O plano está alinhado; ainda não execute”.

Nomeie a versão do plano. Se ele estiver só na conversa, a ordem de execução deve resumir objetivo, escopo, blocos, aceite, verificações e limites de forma suficiente para retomá-lo.

Autorização para implementar localmente não autoriza automaticamente publicar, mexer em banco real, apagar dados ou enviar mensagens. Liste essas ações quando fizerem parte da execução desejada. Se já estiverem autorizadas no plano, a autorização permanece válida dentro daquele escopo.

## 6. Execute e avance pelos blocos

O ciclo de cada bloco é:

1. Fazer a mudança dentro do escopo.
2. Executar a verificação prevista.
3. Corrigir falhas da própria mudança e conferir novamente quando necessário.
4. Registrar um checkpoint curto.
5. Começar automaticamente o próximo bloco aprovado.

Um checkpoint informa **resultado, evidência, limitações relevantes e próximo passo**. Não abre uma nova rodada de aprovação para uma transição já prevista.

Exemplo fictício:

> B01 concluído: a lista começou vazia e recebeu 3 tarefas. Os 3 títulos e a contagem foram conferidos no ambiente local. Vou iniciar B02 para concluir uma tarefa e preservar o estado ao recarregar.

Evite usar quantidade de arquivos ou testes como prova principal. “12 arquivos alterados” não demonstra que o aluno consegue concluir e recuperar uma tarefa.

## 7. Verifique sem criar ciclos inúteis

A verificação precisa combinar com a mudança. Um texto pode exigir revisão e conferência visual. Um pagamento exige conferir cobrança e consequências no fluxo. Uma correção de contagem exige mostrar os números antes e depois.

Defina as verificações no plano e confirme os comandos reais antes de prometê-los. Use cenários que revelam erros relevantes, incluindo condições de falha quando fizerem parte do risco.

Reaproveite evidências válidas. Repita uma verificação quando houver mudança relevante, resultado inconclusivo ou exigência do projeto. Depois de duas tentativas equivalentes sem evidência nova, reavalie a abordagem em vez de repetir a mesma tentativa.

Se uma verificação obrigatória não puder ser feita, registre o impedimento: a entrega continua incompleta nesse critério. Defeito de outra frente deve ser sinalizado; preserve o trabalho de outras pessoas e agentes.

## 8. Pare pelos motivos certos

Continue até concluir o plano, salvo:

- Decisão externa indispensável.
- Risco novo relevante.
- Autorização ainda ausente para ação irreversível ou produção.
- Impedimento real que inviabiliza o próximo trabalho necessário.
- Ampliação material do escopo.

Ao parar, preserve o estado e explique em linguagem simples: o problema, um exemplo concreto, a consequência e uma decisão com recomendação. Informe o que já foi feito e o que falta.

Um ajuste rotineiro dentro do resultado aprovado não exige outra autorização. Uma mudança importante no plano precisa ser apresentada antes de executada.

A estimativa orienta expectativa; não é um teto automático nem uma obrigação de ocupar tempo. Informe desvios relevantes e encerre antes quando terminar. Limites reais da ferramenta ou da conta continuam valendo. “Tokens” são unidades de consumo da IA; não equivalem a horas. Só estabeleça um orçamento numérico se o usuário pedir.

## 9. Proteja trabalhos simultâneos

Em projetos com histórico de versões, confira as alterações locais e remotas nas duas direções antes de editar. Use uma branch de tarefa — uma linha separada de alterações — e um worktree isolado — uma pasta separada para trabalhar sem disputar os mesmos arquivos.

Peça ao agente para fazer isso; você não precisa executar comandos manualmente. Ele deve preservar mudanças existentes e informar conflitos, sem sobrescrever o trabalho de outro agente. Evite commits diretamente na branch principal.

Se houver publicação ou atualização de banco, siga o procedimento específico daquele projeto. Mudanças em números mostrados a clientes, especialmente quedas, exigem alinhamento antes da publicação.

## 10. Feche com entrega comprovada

No fechamento, mostre:

- O resultado demonstrável e onde pode ser conferido.
- O que mudou e as verificações realmente realizadas.
- O ambiente e a versão ou referência, quando aplicável.
- Pendências e limitações, com situação honesta.
- Próximo trabalho recomendado, explicitando quando está fora do plano.

| Situação | O que você pode afirmar |
|---|---|
| Pronto e verificado localmente | Funciona no ambiente local conferido |
| Integrado na branch principal | As alterações entraram no histórico principal |
| Aguardando publicação | A entrega ainda precisa chegar ao ambiente combinado |
| Publicado e verificado | A versão publicada foi conferida no ambiente de destino |

Integrar o código não prova publicação. Em um aplicativo, confira a versão e o fluxo no ambiente publicado. Em documentação no GitHub, confira os arquivos e a navegação no repositório remoto.

Atualize o plano e os registros pertinentes ao corrigir uma pendência: preserve o histórico e acrescente o estado atual e a evidência. Um problema resolvido não deve continuar descrito como pendência atual.

Use o [modelo de fechamento](../modelos/fechamento.md). O plano só está concluído quando as verificações necessárias e a entrega no ambiente combinado estão confirmadas.
