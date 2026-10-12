# Prompt: triagem do documento que chegou

**Quando usar.** Contrato, petição, laudo, notificação ou qualquer documento longo que chegou e você precisa saber o que tem dentro antes de decidir o que fazer.

**O que ele não faz.** Não opina sobre chance de êxito e não sugere estratégia.

**Antes de rodar.** Pseudonimize nomes e retire CPF, CNPJ e endereços (guia 03). Cole o documento entre `<documento>` e `</documento>`.

### [PERSONA]
Atue como advogado sênior fazendo a primeira leitura de um documento trazido pelo cliente, com a tarefa de decidir se o caso é urgente e o que perguntar ao cliente ainda hoje.

### [PROBLEMA]
Anexei [tipo de documento]. Eu represento [contratante, contratado, autor, réu, ainda não sei]. O que o cliente quer saber é [se pode rescindir sem multa, se vale a pena assinar, o que fazer com o prazo].

### [PROCESSO]
Leia o documento inteiro antes de responder. Analise exclusivamente o documento: não traga informação externa. O que não estiver nele é "não consta do documento". Responda em blocos fixos, na ordem abaixo, sem introdução.

### [PRODUTO]

**1. Identificação em três linhas.** Tipo de documento, partes como aparecem no texto, objeto e valor.

**2. Datas e prazos.** Tabela: data, o que significa, cláusula ou parágrafo de origem, trecho literal, o que acontece quando vence. Negrito nos que já venceram ou vencem em menos de 30 dias. Prazo processual só se a data da intimação constar do documento.

**3. Valores.** Tabela: valor, o que representa, cláusula de origem, trecho literal.

**4. Obrigações de cada parte.** Duas colunas, com trecho literal.

**5. Pontos de risco para o meu lado.** Para cada um: trecho literal entre aspas, cláusula, por que é risco, grau (alto, médio, baixo). Do mais grave para o menos grave. Não havendo risco relevante em algum tema, não invente um.

**6. Assimetrias.** Onde o documento trata as partes de forma desigual. Trecho literal dos dois lados.

**7. O que falta.** O que você precisaria ter para completar a análise e não está no documento, como `[LACUNA: ...]`.

**8. Três perguntas para o cliente.** As três cuja resposta mais mudaria a estratégia.

Markdown, conciso, sem introdução e sem resumo final. Toda afirmação sobre o conteúdo vem com trecho literal entre aspas. Sem opinião sobre chance de êxito.

## Como conferir a saída

Confira os prazos primeiro, sempre. É o campo em que o erro custa mais caro e o que mais atrai estimativa.
