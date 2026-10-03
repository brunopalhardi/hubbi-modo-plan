# Prompts para cada momento

[Voltar ao início](../README.md)

Substitua os campos entre colchetes. Revise ações externas, publicação e exclusões antes de enviar. Um pedido para planejar não autoriza implementar.

## 1. Transformar uma ideia em plano

```text
Quero [resultado] para [público]. Hoje [problema], e isso causa [consequência].
Já existe [estado de partida]. Quero conferir o sucesso por [demonstração].

Faça uma inspeção curta e dirigida, reaproveitando evidências válidas.
Antes de implementar, apresente um plano completo por blocos:
- Objetivo, partida, entrega demonstrável e mapa B01 até o fechamento.
- Escopo incluído, exclusões, dependências e autorizações necessárias.
- Resultado, passos, aceite e verificação proporcional em cada bloco.
- Estimativa por bloco e total, sem teto automático de duração.
- Modelo e esforço disponíveis por bloco, motivo, consumo e reavaliação.
- Execução individual ou com subagentes; se delegar, delimite responsabilidades.
- Critérios de parada, ambiente final e texto autossuficiente para execução.

Não inclua [exclusões]. Não implemente nem inicie /goal enquanto eu reviso.
Explique escolhas em linguagem simples e recomende uma decisão por vez.
```

## 2. Ajustar o plano antes de executar

```text
O plano precisa ajustar [ponto]. Quero [resultado corrigido], porque [motivo].
Atualize o mapa completo, os critérios de aceite e as dependências afetadas.
Apresente a versão revisada e aguarde minha autorização de execução.
```

## 3. Aprovar e autorizar todos os blocos

```text
Aprovo e autorizo executar o plano [caminho/nome e versão], de B01 a [último].
O resultado final é [entrega], verificado por [critérios e demonstração].
Entram [escopo]. Ficam fora [exclusões].

Configuração aprovada: [modelo e esforço por bloco], [individual ou delegação
com tarefas, áreas e configuração de cada subagente]. Confirme disponibilidade
e informe qualquer diferença; não troque configurações silenciosamente.

Ações externas/publicação autorizadas: [lista precisa ou “nenhuma”].
Informe checkpoints com resultado, evidência e próximo passo. Avance
automaticamente entre os blocos aprovados, sem pedir novo “ok” a cada transição.
Pare por conclusão, decisão externa indispensável, risco novo relevante,
autorização ausente, impedimento real ou ampliação material do escopo.
Encerre com verificação integrada, ambiente, evidências e pendências.
```

## 4. Usar um objetivo persistente, quando disponível

Use após revisar e autorizar o plano. Confira os recursos do seu ambiente em [configuração](configuracao.md).

```text
/goal Execute de ponta a ponta o plano aprovado [caminho e versão], B01 a [último],
até [resultado verificável]. Respeite [escopo], [exclusões], [configuração
e divisão de responsabilidades] e [limites de ações externas autorizadas].
Verifique [fluxos e ambiente], informe checkpoints e continue automaticamente
entre blocos. Pare nas condições do plano e nos limites reais da ferramenta.
Feche com evidências, situação da publicação e pendências.
```

Se o plano estiver apenas na conversa, inclua suas definições no pedido. Não dependa de “faça aquilo que combinamos” numa conversa sem o contexto.

## 5. Pedir status sem interromper a execução

```text
Informe em poucas linhas o bloco atual, o que já foi demonstrado, o que falta
e qualquer desvio relevante. Continue o plano autorizado depois do status.
```

## 6. Resolver um impedimento

```text
Explique o impedimento em português simples: problema, exemplo concreto,
consequência e detalhe técnico curto. Informe evidências, resultado já obtido
e trabalho necessário restante. Traga uma decisão com recomendação e diga
se a solução cabe no escopo ou exige mudança no plano.
Preserve o estado e o trabalho dos outros agentes.
```

## 7. Retomar em outra conversa

```text
Retome o plano [caminho e versão] a partir do checkpoint [identificação].
Leia as instruções do projeto e o registro de continuidade. Confira o estado
local e remoto antes de editar; preserve alterações de outras frentes.
Reaproveite as evidências válidas e repita somente verificações afetadas,
inconclusivas ou exigidas pelo projeto.

A autorização continua para [blocos e ações já aprovadas]. Falta [resultado].
Mantenha [configuração e responsabilidades] e avance até fechar o plano.
Se encontrar diferença relevante entre o registro e a realidade, informe-a.
```

## 8. Conferir a entrega

```text
Confira os critérios de aceite do plano e mostre o resultado observável.
Informe o que mudou, o que foi realmente verificado e o ambiente/versão.
Separe verificação local, integração e publicação confirmada.
Liste limitações e pendências; não declare conclusão com trabalho obrigatório
restante. Atualize plano e registros pertinentes com o estado atual.
```
