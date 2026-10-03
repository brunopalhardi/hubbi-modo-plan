# Exemplo completo — lista de estudos

[Voltar ao início](../README.md)

**Exemplo fictício e didático.** Nenhum aplicativo foi implementado neste repositório. As mensagens, escolhas e resultados abaixo são uma simulação para ensinar o método. Em seu projeto, substitua por verificações reais.

## 1. Pedido inicial do aluno

> Quero uma lista de estudos no navegador, para acompanhar o que já fiz. Quero adicionar 3 tarefas, concluir 1 e continuar vendo essa conclusão depois de recarregar a página. Começaremos do zero. Monte o plano antes de implementar. Não preciso de login, compartilhamento ou notificações.

O problema está definido: perder o estado das tarefas dificulta acompanhar o estudo. A demonstração usa 3 tarefas e 1 conclusão; o agente já sabe o que precisa preservar.

## 2. Plano apresentado pelo agente

**Plano v1 — acompanhar tarefas de estudo sem perder o progresso ao recarregar**

Objetivo e valor: permitir que um aluno registre tarefas e identifique as concluídas no mesmo navegador.

Partida: projeto novo, sem código ou dados a preservar. Na inspeção inicial, confirmar as ferramentas locais disponíveis e o formato mais simples que o ambiente consegue executar.

Entrega demonstrável: página local, instruções de abertura e percurso conferido com 3 tarefas, 1 concluída e estado preservado após recarregar.

Entra: adicionar tarefa, listar, concluir/desmarcar, contar total e concluídas, rejeitar título vazio e guardar o estado no navegador.

Fora: conta de usuário, banco remoto, vários dispositivos, compartilhamento, excluir tarefas, notificações e publicação na internet.

Dependências: ambiente local e navegador disponíveis; definir o armazenamento local após a inspeção. “Armazenamento local” significa guardar o estado no próprio navegador, como uma gaveta daquele computador.

Limite importante: limpar os dados do navegador pode apagar a lista. O aplicativo é para uso local nesse navegador; cópia de segurança fica fora deste plano.

Autorização proposta: criar arquivos na área isolada e verificar no ambiente local. Sem produção, mensagens, banco real ou publicação externa.

### Mapa completo

| Bloco | Resultado | Dependência | Estimativa ilustrativa |
|---|---|---|---|
| B01 — adicionar e listar | Lista vai de 0 para 3 tarefas | Ambiente local confirmado | 15–25 min |
| B02 — concluir e preservar | 1 concluída permanece ao recarregar | B01 | 15–25 min |
| B03 — conferir e documentar | Fluxo completo validado, com instruções e fechamento | B01 e B02 | 10–15 min |

Total ilustrativo: 40–65 minutos, sem teto automático. São estimativas do exemplo; não constituem medição ou promessa.

### B01 — adicionar e listar

- Passos: preparar a página local → exibir estado vazio → permitir adicionar título → exibir lista e contagem.
- Áreas: página, entrada de texto e apresentação das tarefas.
- Aceite: iniciar com 0; adicionar “Ler capítulo”, “Fazer exercício” e “Revisar notas”; exibir os 3 títulos e total 3.
- Verificação adicional: enviar título vazio ou apenas espaços; total continua 3 e uma orientação aparece.
- Evidência esperada: observação do fluxo no navegador, com registros sem dados pessoais.
- Passagem: B02 recebe uma lista funcional para acrescentar conclusão e persistência.

### B02 — concluir e preservar

- Passos: marcar/desmarcar conclusão → atualizar contadores → salvar estado → recuperar ao recarregar.
- Áreas: comportamento das tarefas e armazenamento no navegador.
- Aceite: concluir “Ler capítulo”; total 3, concluídas 1. Recarregar; mesmos títulos e contadores. Desmarcar; concluídas 0, total 3. Recarregar e conferir novamente.
- Verificação: testar os dois estados e observar o resultado na interface, sem depender apenas de conferir dados internos.
- Evidência esperada: estado antes/depois das recargas e ausência de erro no percurso.
- Passagem: B03 recebe o fluxo pronto para verificação integrada e instruções.

### B03 — conferir e documentar

- Passos: executar o percurso completo em um estado de demonstração controlado → conferir contagens e recargas → escrever instruções de uso → registrar entrega.
- Áreas: fluxo integrado, instruções e fechamento do plano.
- Aceite: os critérios de B01/B02 passam; abertura e limitação de armazenamento estão explicadas; nenhum recurso fora do escopo foi acrescentado.
- Verificação: reaproveitar evidências anteriores que continuam válidas e repetir o fluxo integrado necessário. Não ampliar testes sem risco ou mudança que justifique.
- Evidência esperada: referência do artefato local, resultado do percurso e instruções.

### Configuração e execução

Escolha ilustrativa: execução individual, porque cada bloco depende do anterior e há uma área principal de escrita.

Modelo/esforço: um modelo de uso geral disponível, com raciocínio médio em B01/B02 e baixo em B03. **Num plano real, o agente deve substituir essa descrição pelo nome confirmado no ambiente.** Ela não afirma disponibilidade nem configura um produto.

Motivo: implementação pequena e delimitada, com atenção à recuperação do estado. Reavaliar se a gravação falhar ou surgir dificuldade técnica que não caiba na solução proposta. Apresentar qualquer mudança antes de adotá-la. Mais profundidade e agentes extras só se houver benefício concreto; seu consumo entra no total.

Aceite final: 3 tarefas e seus títulos preservados; 1 conclusão preservada; desmarcação preservada; título vazio rejeitado; instruções corretas; entrega verificada localmente.

Paradas: conclusão, decisão externa indispensável, risco novo relevante, autorização ausente, impedimento real ou ampliação material. Se faltar uma ferramenta obrigatória e não houver caminho equivalente seguro, informar o impedimento e a decisão recomendada.

## 3. Revisão e autorização do aluno

> Aprovo e autorizo a execução do plano v1, B01 a B03, com execução individual e a configuração disponível confirmada antes de começar. Pode criar os arquivos e verificar localmente. Informe checkpoints e avance automaticamente. Não publique nem inclua os recursos que ficaram fora do escopo.

Essa mensagem autoriza todos os blocos. O aluno não precisa enviar “segue” a cada conclusão.

## 4. Checkpoints simulados

### B01

> B01 concluído: a página começou com 0 tarefas. Adicionei os 3 títulos combinados e conferi total 3. O envio vazio foi recusado e a contagem permaneceu 3. Verificação local. Vou iniciar B02 para concluir tarefas e preservar o estado.

### B02

> B02 concluído: “Ler capítulo” ficou concluída; total 3, concluídas 1. Após recarregar, títulos e conclusão permaneceram. Desmarquei, recarreguei e conferi concluídas 0, total 3. Vou iniciar B03 para conferir o fluxo integrado e escrever as instruções.

### B03

> B03 concluído: o percurso integrado passou no cenário de demonstração. As instruções explicam abertura, uso e a possibilidade de perder a lista ao limpar os dados do navegador. Vou registrar o fechamento local.

Todos esses relatos são simulados. Num trabalho real, cada declaração precisa corresponder a uma verificação feita.

## 5. Como lidar com uma mudança no meio

Suponha que o aluno peça, durante B02: “Quero ver a mesma lista no celular e no computador”.

Isso altera o resultado e as dependências: guardar tudo em um navegador já não atende. O agente deve explicar a consequência e propor um ajuste do plano, antes de acrescentar serviço remoto ou autenticação.

Resposta didática:

> A lista atual fica guardada em um navegador. As 3 tarefas criadas no computador não apareceriam automaticamente no celular. Para usar os dois dispositivos, precisamos ampliar o plano e definir como identificar o usuário e guardar os dados compartilhados. Recomendo fechar primeiro a versão local aprovada e planejar essa evolução separadamente.

O aluno decide essa mudança. A autonomia autorizada para a versão local permanece restrita ao plano v1 até esse alinhamento.

## 6. Fechamento simulado

Situação: **concluído e verificado localmente**, neste exemplo.

| Critério | Evidência simulada | Resultado |
|---|---|---|
| Adicionar e listar | 0 → 3 tarefas; títulos conferidos | Aprovado |
| Rejeitar título vazio | Total permaneceu 3 | Aprovado |
| Concluir e recuperar | 3 totais, 1 concluída após recarregar | Aprovado |
| Desmarcar e recuperar | 3 totais, 0 concluídas após recarregar | Aprovado |
| Instruções | Abertura, uso e limite do armazenamento descritos | Aprovado |

Mudanças: página local, comportamento de tarefas, armazenamento e instruções. Versão/referência: num projeto real, preencher a referência existente do artefato ou commit.

Publicação: não autorizada nem realizada; o aceite final combinado era local. Pendências obrigatórias: nenhuma na simulação. Limitações: sem sincronização entre dispositivos e possível perda ao limpar os dados do navegador.

Registros: plano v1, checkpoints e fechamento atualizados na simulação. Uma versão para vários dispositivos é um próximo trabalho fora deste plano.

## 7. Exercício para o aluno

Peça a um agente um plano para essa lista. Antes de autorizar, confira:

- O mapa mostra o percurso completo e suas dependências?
- Cada bloco termina em algo que você consegue conferir?
- Os nomes de modelo e níveis foram confirmados no seu ambiente?
- Publicação, dados reais e recursos extras estão delimitados?
- A ordem de execução cobre os blocos e define quando parar?

Após executar no seu projeto, use evidências reais para preencher o [checkpoint](../modelos/checkpoint.md) e o [fechamento](../modelos/fechamento.md). Se algo obrigatório não foi verificado, registre como pendente.
