# Prompt: contrato a partir de briefing

**Quando usar.** O cliente descreveu o que quer, por e-mail, áudio transcrito ou conversa anotada, e você precisa da primeira minuta.

**O que ele não faz.** Não entrega minuta pronta para assinatura. Entrega uma minuta com as lacunas expostas, para você fechar.

**Antes de rodar.** Pseudonimize o que identifica (nomes viram papéis, CPF e endereço saem; veja `01-guias/03_guia_dados_pessoais.md`). Anexe ao projeto o padrão de cláusulas do escritório, se houver: é ele que impede a IA de inventar cláusula "de mercado".

São quatro etapas. Não pule para a etapa 3, e não assine sem a etapa 4.

**Para contrato de honorários**, use a variação pronta em `11_contrato_de_honorarios.md`.

**Delimite o material.** Cole o briefing entre `<briefing>` e `</briefing>`. Veja `01-guias/04_guia_texto_estruturado.md`.

## Etapa 1: leitura do briefing

### [PERSONA]
Atue como advogado especialista em direito contratual com vinte anos de prática, acostumado a redigir contratos que já foram testados em litígio, revisado por um sócio que litigou contratos parecidos e sabe onde eles quebram.

### [PROBLEMA]
Anexei o briefing do cliente. Preciso entender o que já está definido e o que ainda falta para que a minuta seja redigida sem invenção. O objetivo do contrato é [uma frase: o que cada parte entrega e o que cada uma recebe], e o meu cliente é [parte].

### [PROCESSO]
Não redija nenhuma cláusula nesta etapa. Primeiro, liste em tabela o que o briefing já define: partes, objeto, prazo, preço e forma de pagamento, obrigações de cada parte, garantias, hipóteses de rescisão, multa, foro. Depois, o que não está definido e é indispensável. Por fim, no máximo cinco perguntas objetivas, ordenadas pelo risco de errar se eu não responder.

### [PRODUTO]
Tabela com três colunas: elemento, o que o briefing diz, trecho literal do briefing. Elemento ausente fica como `[LACUNA]`. Não sugira redação de cláusula nesta etapa.

## Etapa 2: esqueleto de cláusulas

### [PERSONA]
Mantenha a persona anterior.

### [PROBLEMA]
Com base no briefing e nas minhas respostas, preciso validar a arquitetura do contrato antes de qualquer redação, para não descobrir na décima cláusula que a estrutura está errada.

### [PROCESSO]
Escreva apenas a lista de cláusulas na ordem em que aparecerão, cada uma com um parágrafo curto explicando o que vai dizer e por que está no contrato. Não redija texto contratual.

### [PRODUTO]
Lista numerada. Marque com `[RISCO]` as cláusulas que protegem o meu cliente de um risco específico, dizendo qual. Marque com `[LACUNA]` as que dependem de informação que ainda não tenho. Não inclua cláusula só porque é comum no mercado: toda cláusula precisa vir do briefing, das minhas respostas ou do padrão do escritório anexado ao projeto.

## Etapa 3: redação, cláusula a cláusula

### [PERSONA]
Mantenha a persona anterior.

### [PROBLEMA]
Redija a cláusula [número e nome], conforme aprovada no esqueleto.

### [PROCESSO]
Uma cláusula por vez. Se tiver parágrafos ou incisos, use a estrutura usual do escritório. Ao final, aponte em uma linha o que essa cláusula deixa desprotegido.

### [PRODUTO]
Texto contratual em português culto jurídico, sem adjetivação. Sem citar jurisprudência ou doutrina. Artigo de lei só quando eu pedir e sempre com `[VERIFICAR]`. Informação que faltar entra como `[LACUNA: o que falta]` dentro do texto, nunca preenchida por conta própria. Não invente valores, prazos, índices de correção nem nomes.

## Etapa 4: rodada de crítica e brainstorm (você no comando)

Antes de assinar, uma rodada em que a IA ataca a minuta e propõe alternativas. Quem decide é você.

### [PERSONA]
Atue como três leitores, um de cada vez: o advogado da outra parte, o cliente leigo que vai assinar, e o juiz que vai interpretar a cláusula numa disputa daqui a dois anos.

### [PROBLEMA]
Colei a minuta que redigimos. Preciso saber onde ela é frágil antes de assinar, e ver alternativas de redação para os pontos fracos, para escolher entre elas.

### [PROCESSO]
Primeiro, apenas a crítica: para cada leitor, os três pontos mais frágeis, cada um com o trecho da minuta. Pare. Depois que eu escolher quais pontos quero trabalhar, proponha três redações alternativas para cada um, dizendo o ganho e o custo de cada uma. Não reescreva a minuta inteira e não escolha por mim.

### [PRODUTO]
Crítica em tabela: leitor, ponto frágil, trecho literal da minuta, por que é frágil. Alternativas em blocos separados, sem citar jurisprudência ou doutrina. Informação que faltar entra como `[LACUNA]`. No final, uma linha para eu registrar a decisão: o que aceitei, o que rejeitei e por quê.

## Como conferir a saída da etapa 4

Verifique se a crítica aponta trecho que existe na minuta. Depois leia as alternativas como se a IA estivesse tentando agradar: ela tende a propor cláusulas mais favoráveis do que o razoável. O que você não escolheu não entra no texto. Cada rodada vira uma versão do documento; guarde a decisão registrada.

## Como conferir a saída das etapas 1 a 3

Leia procurando três coisas: cláusula que você não pediu e não está no padrão do escritório; número, prazo ou índice que você não forneceu; e obrigação atribuída a uma parte que o briefing atribuía à outra. São os três erros mais frequentes nesta tarefa.
