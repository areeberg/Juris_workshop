# Prompt: red team

**Quando usar.** Duas situações. A peça da parte contrária chegou e você vai contestar ou replicar. Ou a sua peça está pronta e você tem uma hora antes do protocolo.

**Por que é o prompt mais seguro do kit.** A IA trabalha só em cima do documento que você deu, e a exigência de trecho literal fecha o espaço para alucinação.

**Versão em habilidade:** `04-habilidades/advogado-do-diabo/`.

**O que ele não faz.** Não reescreve a peça. Entrega uma lista de brechas para você decidir o que fechar.

### [PERSONA]
Atue como advogado adversarial agindo a meu favor: experiente, bem pago para derrubar esta peça, sem nenhum compromisso em ser gentil. Você vai atrás do ponto mais barato de atacar, não do mais elegante.

### [PROBLEMA]
Anexei [a peça da parte contrária / a peça que pretendo protocolar] e os documentos que a instruem. Eu represento [autor / réu]. Fatos que eu tenho e o documento não menciona: [opcional, mas ajuda muito]. Interessa especialmente o que pode ser atacado sem produção de prova nova.

### [PROCESSO]
Primeiro apenas a lista de ataques, ordenada pela probabilidade de funcionar, sem desenvolver nenhum. Vou escolher quais quero detalhados. Só então desenvolva os escolhidos, um por vez.

### [PRODUTO]

**Regra obrigatória de evidência.** Para cada ponto apontado, transcreva entre aspas o trecho literal do documento que o sustenta, indicando página ou parágrafo. Se não conseguir localizar um trecho literal que sustente o ponto, não aponte o ponto. Um defeito que você não consegue citar é um defeito que você inventou.

Entregue nesta ordem:

**1. Preliminares e questões processuais.** Para cada uma: trecho literal, o vício, e o dispositivo aplicável com `[VERIFICAR]`.
- Inépcia: pedido indeterminado, falta de causa de pedir, incompatibilidade entre pedidos
- Prescrição ou decadência, com base nas datas que aparecem no próprio documento
- Ilegitimidade de parte, ativa ou passiva
- Incompetência do juízo
- Falta de interesse de agir
- Ausência de documento indispensável mencionado mas não juntado

**2. Contradições internas.** Cite os dois trechos conflitantes, lado a lado.

**3. Alegações sem lastro.** Afirmações não amparadas em documento citado na peça. Trecho literal e qual prova faltaria.

**4. O elo mais fraco.** Um parágrafo: se você tivesse um único argumento, qual seria e por quê.

**5. Três teses de defesa.** Argumento em duas linhas, fundamento legal com `[VERIFICAR]`, provas necessárias para sustentá-la.

**6. O que eles fizeram bem.** Os dois pontos mais fortes da peça, para eu não subestimar. Seja honesto aqui.

**Lista separada, "não verificável com o que está na mesa":** ataques que dependem de documento não anexado. Não entram na lista principal.

Sem citar jurisprudência, súmula ou doutrina. Ataque que só funcione com precedente vira `[FALTA PRECEDENTE: o que preciso encontrar]`. Não resuma o que a parte disse, vá direto ao ataque.

## Como conferir a saída

Confira o trecho literal de cada ataque. O erro típico é apontar contradição entre dois pontos que, lidos por inteiro, não se contradizem. Se o trecho citado não estiver na peça, descarte o ataque inteiro e desconfie dos demais.

## Variação: contra a sua própria peça, antes de protocolar

Mesmo prompt, trocando o Problema: "anexei a peça que eu pretendo protocolar; preciso saber por onde ela cai antes que o outro lado descubra". No Produto, acrescente a cada ataque uma linha com o que eu preciso fazer para fechar a brecha. É o uso de maior retorno do kit inteiro e o que menos gente faz.
