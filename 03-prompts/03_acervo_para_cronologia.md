# Prompt: do acervo à cronologia dos fatos

**Quando usar.** O cliente entregou um volume de documentos, ou você recebeu os autos, e precisa saber o que aconteceu, quando, e provado por qual documento.

**O que ele não faz.** Não analisa mérito nem sugere tese. Isso vem depois, com a cronologia já validada.

**Antes de rodar.** Pseudonimize (guia 03). Separe os documentos em lotes e processe um lote por vez, conferindo antes de seguir. Fatiar não é limitação da ferramenta, é o que cria o seu ponto de conferência.

### [PERSONA]
Atue como assessor de escritório encarregado de montar a cronologia auditável de um caso, do tipo que o sócio confere por amostragem e não encontra erro.

### [PROBLEMA]
Anexei [contrato, notificações, laudo, prints de conversa, autos]. Preciso saber o que aconteceu, em que ordem, e qual documento prova cada fato, para depois decidir a tese. Meu cliente é [parte] e a questão em disputa é [uma frase].

### [PROCESSO]
Processe apenas os documentos deste lote. Não misture com o que vier depois. Ao terminar, pare e apresente o resultado para conferência antes de continuar. Não interprete o mérito, não classifique quem tem razão, não antecipe tese.

### [PRODUTO]
Três entregas, nesta ordem.

Primeira, tabela cronológica com as colunas: data, fato, documento e página, trecho literal entre aspas. Data que não constar do documento entra como "sem data no documento", nunca estimada.

Segunda, tabela de provas com as colunas: fato a provar, documento que prova, força da prova (direta, indireta, apenas indiciária), o que enfraquece essa prova.

Terceira, lista de lacunas: fatos que o caso pressupõe e que nenhum documento deste lote comprova, cada um como `[FATO A CONFIRMAR: ...]`.

Nada fora dos documentos anexados. Fato que apareça em dois documentos com versões diferentes: registre as duas, marque como contradição, não escolha.

**Exemplo para treinar:** a pasta `caso-ficticio-dona-marta/` traz um dossiê de exemplo com páginas numeradas. Rode este prompt nele antes de rodar em caso real.

## Como conferir a saída

Escolha três linhas da tabela ao acaso e confira o trecho literal na página indicada. Se as três baterem, a tabela costuma estar íntegra. Confira sempre as datas mais antigas, que são as que mais viram estimativa disfarçada.
