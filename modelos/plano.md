# Plano — [resultado final desejado]

> Modelo para copiar. Preencha os campos; acrescente ou remova blocos conforme a demanda. Não inicie a execução só porque o plano foi escrito.

Data: [data] · Versão: [v1] · Estado: [proposto / aprovado / execução autorizada / em execução / parcial / concluído]

## Objetivo e partida

- **Objetivo e valor:** [o que passa a ser possível, para quem e por quê].
- **Estado de partida:** [o que existe, evidências reaproveitadas e lacunas relevantes].
- **Entrega final demonstrável:** [fluxo, tela, documento ou evidência que será mostrado].
- **Ambiente final combinado:** [local / ambiente de prévia / produção / repositório público].

## Escopo, dependências e autorizações

- **Entra:** [lista fechada de mudanças e áreas].
- **Não entra:** [exclusões e futuros trabalhos].
- **Dependências:** [acessos, ferramentas, decisões e serviços].
- **Ações externas e publicação autorizadas:** [lista precisa ou nenhuma].
- **Autorizações ainda necessárias:** [ação e momento; nenhuma se todas concedidas].
- **Preservação e isolamento:** [trabalho existente a preservar, branch e área isolada].

## Mapa completo

| Bloco | Resultado observável | Depende de | Estimativa |
|---|---|---|---|
| B01 — [início] | [resultado] | [partida] | [faixa] |
| B02 — [meio] | [resultado] | [B01 ou outra dependência] | [faixa] |
| B03 — [fechamento] | [entrega integrada] | [blocos anteriores] | [faixa] |

Estimativa total: [faixa]; orienta expectativa, sem teto automático ou espera artificial.

## Detalhe de cada bloco

### B01 — [nome orientado ao resultado]

- Objetivo verificável e resultado: [descrição].
- Passos: [ação → resultado → verificação].
- Áreas envolvidas: [telas, arquivos, banco, serviço ou documento].
- Dependências e autorização: [o que precisa estar disponível].
- Aceite: [condições observáveis e suficientes].
- Verificação: [fluxo/comando real, ambiente, evidência esperada].
- Evidências reaproveitadas: [quais e por que continuam válidas].
- Modelo e esforço: [nomes disponíveis, justificativa, qualidade/velocidade/consumo].
- Reavaliar configuração se: [condição concreta; mudança apresentada antes].
- Próximo bloco: [qual resultado B01 entrega para ele].

Repita o detalhe para B02…BXX, incluindo integração e fechamento.

## Execução individual ou delegada

Escolha: [individual / coordenador e até dois subagentes]. Justificativa: [ganho concreto ou dependência que favorece execução individual].

Se delegar, preencher uma linha por subagente:

| Agente | Tarefa independente e entradas | Resultado | Área permitida e isolamento | Modelo/esforço | Parada |
|---|---|---|---|---|---|
| [identificação] | [tarefa] | [evidência] | [área sem sobreposição] | [disponíveis] | [condição] |

Integração e verificação pelo coordenador: [procedimento]. Expansão ou subdelegação: [somente se explicitamente aprovada].

Confirmação de configuração: [opções disponíveis e seleção efetiva, quando verificável]. A recomendação não prova que o aplicativo mudou de modelo/esforço.

## Aceite final e paradas

- [Condição 1 do resultado integrado].
- [Condição 2 e demonstração no ambiente combinado].
- [Registros, instruções e pendências atualizados].

Parar por conclusão; decisão externa indispensável; risco novo relevante; autorização ausente para ação irreversível/produção; impedimento real; ampliação material do escopo. Ajustes rotineiros dentro do resultado aprovado continuam. Limites reais da ferramenta/conta permanecem válidos.

## Aprovação e autorização de execução

- Versão aprovada: [versão].
- Autorizado por/data: [registro].
- Blocos, configuração, delegação e ações externas abrangidos: [descrição].

## Texto pronto para execução ou /goal, quando disponível

```text
Execute de ponta a ponta o plano [caminho e versão], B01…BXX, até [resultado].
Entram [escopo]; ficam fora [exclusões]. Verifique [critérios, fluxos e ambiente].
Use [modelo/esforço por bloco] e [individual ou responsabilidades delegadas].
Confirme opções disponíveis e informe diferenças de configuração.
Autorizações externas/publicação: [lista ou nenhuma].
Informe checkpoints e avance automaticamente entre blocos aprovados.
Pare nas condições do plano; feche com evidências, ambiente e pendências.
```

## Checkpoints e fechamento

Durante a execução, registrar resultado/evidência/próximo passo por bloco. No encerramento, preencher o [modelo de fechamento](fechamento.md) e manter o estado deste plano coerente com a entrega.
