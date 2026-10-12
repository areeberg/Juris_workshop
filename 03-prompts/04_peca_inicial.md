# Prompt: rascunho de petição inicial

**Quando usar.** Você já ouviu o cliente e precisa da primeira versão estruturada.

**Aviso.** É o prompt de maior risco do kit, o único em que a IA produz fundamentação. Rode sempre dentro do projeto com as instruções coladas, trabalhe em duas etapas e aplique o checklist antes de protocolar.

**Antes de rodar.** Pseudonimize o relato (guia 03). Liste os documentos que você já tem em mãos.

## Etapa 1: estrutura e teses

### [PERSONA]
Atue como advogado sênior brasileiro em contencioso [cível, trabalhista, consumerista, previdenciário], acostumado a peças que magistrado sobrecarregado consegue ler, revisado por sócio que devolve tudo que não sustenta conferência.

### [PROBLEMA]
Colei abaixo o relato do cliente e a lista de documentos que tenho. Preciso decidir a arquitetura da peça e a tese antes de escrever qualquer linha de fundamentação. Meu cliente é [parte] e o resultado prático que ele quer é [uma frase].

RELATO: [cole a transcrição do áudio ou as suas anotações, pseudonimizadas]
DOCUMENTOS EM MÃOS: [contrato, prints, laudo, CTPS, extrato]

### [PROCESSO]
Não redija a peça. Entregue apenas: a tese principal nomeada, as teses subsidiárias, e a estrutura de tópicos da peça, com um parágrafo explicativo por tópico. Depois, pare para eu validar.

### [PRODUTO]
Antes das teses, três seções curtas: **lacunas de informação**, ordenadas por quanto atrapalham a peça; **provas a produzir**, dizendo para cada fato controvertido qual prova o sustenta e o que eu preciso providenciar; **riscos da tese**, em três linhas, onde essa ação pode naufragar. Se a tese que eu quero for fraca, diga antes de tudo.

## Etapa 2: redação

### [PERSONA]
Mantenha a persona anterior.

### [PROBLEMA]
Com a estrutura validada, redija [a peça inteira, ou o tópico X].

### [PROCESSO]
Se a peça for longa, um tópico por vez. Fatos primeiro, sempre.

### [PRODUTO]
A peça deve conter, nesta ordem:

1. **Endereçamento** entre colchetes para preenchimento.
2. **Qualificação das partes** com campos padronizados em branco.
3. **Dos fatos.** Narrativa cronológica, persuasiva e técnica. Destaque em negrito os fatos que geram o direito. Sem juízo de valor exagerado e sem adjetivação. Use apenas fatos do relato. Fato essencial faltando vira `[FATO A CONFIRMAR: ...]`.
4. **Do direito.** Tese principal nomeada, teses subsidiárias, base legal com toda citação marcada `[VERIFICAR]`. Onde couber precedente, escreva `[INSERIR JULGADO AQUI]`. Não produza número de processo, ementa ou nome de relator em nenhuma hipótese.
5. **Dos pedidos.** Lista clara, verbos corretos, tutela de urgência se os fatos sustentarem, honorários de sucumbência, justiça gratuita se cabível.
6. **Valor da causa.** Indique o critério aplicável ao tipo de ação (proveito econômico pretendido, soma das parcelas, valor do contrato) e deixe o cálculo em branco.

Markdown, linguagem moderna e clara, sem arcaísmo, foco em legibilidade para o magistrado.

## Como conferir a saída

Procure primeiro por afirmação de fato que você não contou. É o erro que passa despercebido porque a narrativa fica melhor com ele. Depois resolva todos os colchetes: nenhum sai no protocolo.
