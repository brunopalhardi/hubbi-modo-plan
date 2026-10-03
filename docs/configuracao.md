# Configuração, modelos e instruções do agente

[Voltar ao início](../README.md)

## Aplique sem depender de um comando

Comece em uma conversa com o agente e descreva o resultado. Peça o plano antes da implementação, revise e autorize a execução. Os [prompts](prompts.md) funcionam como pedidos em linguagem natural.

No Codex, recursos de planejamento e objetivos persistentes podem apoiar esse fluxo. Quando disponíveis na sua interface, use o modo de planejamento para alinhar o caminho e `/goal` para manter um objetivo verificável ao longo da execução. Confira a disponibilidade e os controles na [documentação oficial sobre trabalho prolongado](https://learn.chatgpt.com/docs/long-running-work).

Uma ordem com `/goal` deve definir o resultado, como verificá-lo e as restrições; isso corresponde à orientação oficial de [uso de Goals no Codex](https://developers.openai.com/cookbook/examples/codex/using_goals_in_codex). A aprovação única e os blocos deste guia são a organização adotada pela Hubbi.

Exemplo, depois de autorizar o plano:

```text
/goal Execute o plano aprovado plano/lista-de-estudos-v1.md, B01 a B03,
até verificar localmente a inclusão de 3 tarefas, a conclusão de 1 e a
preservação ao recarregar. Informe checkpoints e avance entre blocos.
Não publique nem adicione login, banco remoto ou notificações.
Respeite a configuração individual aprovada no plano e registre o fechamento.
```

O agente deve respeitar os controles e limites reais do ambiente. O método não inicia objetivos, tarefas agendadas ou agentes extras pela mera menção a esses recursos.

## Escolha modelo e profundidade por bloco

**Modelo** é a capacidade escolhida, como selecionar a ferramenta adequada para um serviço. **Esforço de raciocínio** é a profundidade de análise, como decidir quanto revisar uma solução antes de agir. Nenhum dos dois é uma promessa de duração.

| Trabalho | Ponto de partida para a recomendação |
|---|---|
| Claro, repetitivo e de baixo risco | Modelo econômico adequado, com raciocínio baixo ou médio |
| Implementação delimitada e com padrões existentes | Modelo de uso geral, com raciocínio médio |
| Arquitetura, investigação difícil ou regra crítica | Modelo mais capaz, com raciocínio alto quando justificado |

O agente deve preencher o plano com **nomes e níveis realmente disponíveis**, justificar a escolha e explicar a troca entre qualidade, velocidade e consumo. Uma opção barata por chamada pode consumir mais no total se exigir retrabalho.

Peça uma condição de reavaliação: ambiguidade nova, dificuldade imprevista ou resultado insuficiente. Max/Ultra não são padrão; exigem um motivo concreto. Escopo confuso deve ser esclarecido antes de aumentar o esforço.

A recomendação registrada no plano não altera a configuração do aplicativo. Confirme a seleção antes de iniciar e informe qualquer diferença. Se o agente não puder trocar a própria configuração, ele deve orientar você e ser honesto sobre essa limitação.

O modelo escolhido explicitamente pelo usuário prevalece. Em outro produto, como Claude Code, confirme as opções reais daquele ambiente; nomes de modelos do Codex não são configurações transferíveis.

## Decida sobre subagentes

Subagentes são assistentes com tarefas delimitadas coordenados pelo agente principal. Podem ajudar quando há trabalho independente: por exemplo, um analisa uma integração e outro revisa critérios de aceite, cada um com um resultado distinto.

Recomendação padrão: execução individual. Quando houver ganho concreto, planeje **um coordenador e até dois subagentes**, respeitando limites menores do ambiente. Essa divisão precisa estar no plano autorizado; expansão ou subdelegação exige ajuste explícito.

Para cada subagente, defina:

- Tarefa e entradas mínimas necessárias.
- Resultado verificável e condição de parada.
- Área ou arquivos em que pode atuar, sem sobreposição de escrita.
- Modelo e esforço de raciocínio disponíveis.
- Como o coordenador integra e confere o resultado.

Evite duplicar a mesma investigação ou teste. Uma revisão independente pode fazer sentido por risco, desde que tenha foco distinto. Se a escrita não puder ser separada com segurança, mantenha um único escritor.

O coordenador responde pela integração e pela demonstração final. Consumo total inclui todos os agentes; trabalhar em paralelo não garante economia.

## Leve as instruções para seu projeto

O [modelo de AGENTS.md](../modelos/AGENTS.md) contém uma versão reutilizável do método. No Codex, esse tipo de arquivo registra instruções do projeto; a descoberta e a precedência estão descritas na [documentação oficial](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

Peça ao agente:

```text
Leia as instruções existentes neste projeto. Use o modelo AGENTS.md do
hubbi-modo-plan para propor a inclusão do método de planejamento por blocos.
Preserve as regras existentes, sinalize conflitos e adapte apenas o necessário.
Antes de gravar, mostre a proposta para eu revisar.
```

Num projeto novo, o modelo pode virar a base das instruções. Num projeto existente, integre-o cuidadosamente. Ajuste idioma, caminhos, regras de publicação e ambiente de validação. Remova os campos pendentes depois de preenchê-los.

Em outro agente, confirme o mecanismo de instruções reconhecido por ele e use o mesmo conteúdo adaptado. Você também pode colar o método na conversa; nesse caso, reapresente o contexto em uma conversa nova.

## Fontes e atualização

Referências oficiais conferidas em **03/10/2026**. Consulte novamente quando a interface, a versão ou a disponibilidade de recursos mudar:

- [Trabalho prolongado no Codex](https://learn.chatgpt.com/docs/long-running-work).
- [Uso de Goals no Codex](https://developers.openai.com/cookbook/examples/codex/using_goals_in_codex).
- [Instruções com AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

O guia preserva o método independentemente do catálogo de modelos do momento.
