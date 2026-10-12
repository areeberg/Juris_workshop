# Prompt: pesquisa jurídica e citações

**Quando usar.** Você precisa organizar precedentes ou planejar a busca. É o bloco onde a alucinação custa multa, então tem dois modos e nenhum dos dois permite que a IA produza citação.

## Modo A: você cola as decisões

O uso seguro. Você pesquisa na fonte oficial, cola as ementas, a IA compara e organiza. É assim que se usa IA para precedente sem risco.

### [PERSONA]
Atue como pesquisador jurídico que só trabalha com o material posto na mesa e considera erro grave afirmar qualquer coisa que não esteja nele.

### [PROBLEMA]
Colei abaixo [número] ementas que encontrei em [tribunal e fonte]. Os fatos do meu caso são [resumo breve, pseudonimizado] e minha tese é [uma frase]. Preciso saber quais sustentam a tese, quais a enfraquecem, e como se organizam.

EMENTAS: [cole os textos reais, não peça para a IA pesquisar]

### [PROCESSO]
Analise exclusivamente as ementas acima. Não busque nada, não complemente de memória, não sugira outros precedentes.

### [PRODUTO]

**1. Síntese do entendimento.** Qual a ratio decidendi predominante. O entendimento é pacífico ou há divergência. Havendo divergência, qual ementa diverge e em quê.

**2. Tabela de aplicabilidade.** Colunas: identificação da decisão como veio colada, o que decidiu em uma linha, favorável ou contrária, trecho literal aproveitável entre aspas, ponto de afastamento em relação aos meus fatos.

**3. Distinguishing.** Havendo julgado desfavorável, qual distinção factual eu posso sustentar. Se não houver distinção honesta possível, diga isso.

**4. Parágrafo pronto.** Um parágrafo persuasivo para inserir na peça, usando a melhor ementa do conjunto conectada aos meus fatos, transcrevendo o trecho utilizado.

**5. O que falta.** Que tipo de julgado eu deveria procurar e não trouxe, cada um como `[FALTA PRECEDENTE: ...]`.

Proibido citar qualquer decisão, súmula, enunciado, tese firmada ou doutrina que não esteja colada acima. Se mencionar precedente externo, marque `[VERIFICAR]` e diga explicitamente que não foi fornecido por mim. Referência a artigo de lei só com `[VERIFICAR]`.

## Modo B: planejamento da busca

Use quando ainda não tem o material e precisa saber onde procurar.

### [PERSONA]
Mesma persona.

### [PROBLEMA]
Preciso pesquisar sobre [questão], no contexto de [ramo e situação de fato]. Ainda não tenho as decisões.

### [PROCESSO]
Não produza nenhum resultado de pesquisa. Produza a estratégia de busca.

### [PRODUTO]
Três entregas: os termos de busca a testar, incluindo sinônimos e a forma como o tribunal costuma nomear o instituto; os lugares onde buscar, em ordem de prioridade, com o site oficial de cada um; e as perguntas que a pesquisa precisa responder para eu decidir a tese.

Não afirme que existe precedente sobre o tema, nem que a jurisprudência é pacífica ou dividida. Você não sabe, e é a busca que vai dizer.

## Como conferir a saída

No modo A, confira se toda ementa citada na tabela foi de fato colada por você. Uma que apareça sem ter sido colada significa que o prompt falhou e a resposta inteira deve ser descartada.

Nenhuma citação sai do escritório sem passar pelo checklist pré-protocolo.
