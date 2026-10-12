# Guia de sobrevivência: IA no direito

Manual de bolso para usar inteligência artificial no dia a dia da advocacia sem criar risco ético, disciplinar ou processual. Sete regras. Leia uma vez inteiro, depois use como consulta.

Versão de outubro de 2026. Substitui o guia da raiz do repositório, que continha erro sobre ferramentas locais.

## 1. O critério de sigilo não é o preço, é a configuração e o contrato

Circula a ideia de que ferramenta gratuita usa seus dados e ferramenta paga não usa. **Isso não é uma regra confiável.** Existem planos gratuitos com desligamento de treinamento nas configurações, e planos pagos de consumidor sem qualquer garantia contratual sobre uso dos dados.

O que checar, hoje, na ferramenta que você usa:

1. Nas configurações da conta, existe opção de treinamento ou "melhoria do modelo"? Está desligada?
2. O seu plano tem contrato empresarial com cláusula de não uso para treinamento? Plano de consumidor normalmente não tem.
3. A política de retenção diz por quanto tempo o histórico fica armazenado?

### Aplicação local não é processamento local

Esta é a confusão mais cara do mercado hoje, e ela aparece em material sério.

Uma ferramenta de IA pode ser instalada no seu computador, aparecer como aplicativo, pedir autorização para acessar uma pasta sua e mesmo assim **enviar tudo que lê para o servidor do fornecedor**. O que roda na sua máquina é a interface e o acesso ao arquivo. O raciocínio acontece na nuvem, porque é lá que o modelo está.

Duas consequências práticas:

- Autorizar uma pasta controla **o que a ferramenta vê**, não **para onde o conteúdo vai**.
- Qualquer promessa do tipo "roda local, então é seguro" precisa ser conferida antes de você subir documento sigiloso. Quase nenhuma ferramenta popular de IA roda de fato no seu computador.

Correção específica em relação a versões anteriores deste guia: o Google Antigravity não é ferramenta local. É ambiente agêntico apoiado em modelos na nuvem, e no plano gratuito as interações são usadas para treinamento. A mesma advertência vale para qualquer agente de IA instalado na máquina, inclusive os que gerenciam seus arquivos.

### Não encadeie ferramentas de IA

Circula um padrão de uso em que a IA navega até outro site de IA, faz uma pergunta lá, colhe a resposta e transforma em peça. São duas gerações encadeadas sem conferência humana no meio, e os dados do seu caso saem para um terceiro com quem o escritório não tem contrato. Não faça. É exatamente o oposto da supervisão humana efetiva que a OAB exige.

## 2. Anonimize sempre, mesmo em ferramenta paga

Anonimizar custa 30 segundos e elimina a maior parte do problema. E funciona: a IA não precisa saber quem é o João para escrever bem sobre o que aconteceu com ele.

**Nunca cole:** nome completo do cliente ou da parte contrária, CPF, CNPJ, RG, endereço, número de processo em segredo de justiça, valor de acordo confidencial, laudo médico identificado, dados de menor.

**Cole assim:** "O cliente [C], funcionário da empresa [E] desde 2019, sofreu acidente em maio de 2024 e fraturou a perna. A empresa negou o nexo."

**Depois:** troque de volta no Word, não no chat.

O nome técnico do que você está fazendo é **pseudonimização**, e não anonimização: a tabela de correspondência existe e continua sendo dado pessoal. O guia `03_guia_dados_pessoais.md` explica a diferença, as quatro boas práticas e o que é ZDR (retenção zero), que é contratual e não está disponível em plano de consumidor.

## 3. Ela não busca, ela prevê. Por isso inventa

Um modelo de linguagem produz o texto com maior probabilidade de parecer certo. Não existe consulta a banco de dados por trás, a não ser que a ferramenta tenha busca ativa e diga isso explicitamente.

O padrão do erro é sempre o mesmo:

| Ela é confiável em | Ela é perigosa em |
|---|---|
| Estrutura de peça | Número de processo |
| Clareza e redação | Número e conteúdo de súmula |
| Ordenar fatos cronologicamente | Artigo de lei |
| Resumir documento que você deu | Data de vigência |
| Achar contradição em texto que você deu | Valor, nome de parte |

**A inversão que resolve:** nunca peça referência, sempre forneça referência.

Errado: *"busque jurisprudência sobre inscrição indevida"*.
Certo: *"leia estas cinco ementas que eu pesquisei no tribunal e escreva um parágrafo conectando-as com os fatos do meu caso"*.

## 4. O método: quatro partes e trabalho em etapas

Prompt bom não é prompt comprido. É prompt com quatro partes.

**Persona.** Quem está escrevendo. Sem isso a IA assume a média da internet.
**Problema.** Qual resultado jurídico prático você quer, e o que usar ou ignorar do que já foi conversado.
**Processo.** Como o trabalho deve ser executado. Quase sempre: primeiro o esqueleto para você validar, depois cada parte separadamente.
**Produto.** Formato, tamanho, tom e proibições. É a parte que impede a alucinação, e é a que quase todo mundo esquece.

Para ver onde essas peças ficam guardadas (projeto, regras, habilidade, memória, contexto do escritório e da pessoa), leia `05_guia_harness.md`. Para escrever o prompt com marcadores claros, `04_guia_texto_estruturado.md`.

O kit de prompts que acompanha este guia já vem nesse formato, e a folha `03-prompts/10_regra_do_produto.md` traz o bloco de proibições pronto para colar em qualquer prompt seu.

**Trabalho em etapas.** Não entregue o processo inteiro pedindo a peça pronta. Fatie: primeiro a cronologia dos fatos, você confere; depois as teses, você escolhe; depois cada tópico, um por vez. O motivo não é a ferramenta não aguentar o volume, é você precisar de um ponto de conferência a cada etapa. Quem valida a cronologia antes de discutir tese não protocola tese construída sobre fato errado.

## 5. Protocolo de verificação pré-protocolo

Três passos. Cinco minutos por peça. Sempre, mesmo quando a resposta parecer óbvia. A folha completa está no kit, em `03-prompts/09_checklist_pre_protocolo.md`.

**Passo 1, normas.** Toda lei, artigo, súmula, enunciado ou orientação citada: abrir a fonte oficial e conferir número e conteúdo. Atenção especial ao caso em que o número existe e o conteúdo está trocado, que é o erro mais difícil de pegar.

**Passo 2, precedentes.** Todo número de processo e toda ementa: conferir no site do próprio tribunal. Não confie em repositório secundário para confirmar existência.

**Passo 3, fatos.** Toda afirmação sobre datas, valores, partes e documentos: conferir contra o documento que você anexou. Se a IA afirma algo que não está no documento, ela inventou.

**Trava que faz os passos 1 e 2 ficarem baratos:** instrua a IA a marcar com `[VERIFICAR]` toda referência normativa ou jurisprudencial que não tenha vindo de documento fornecido por você. Isso está nas instruções de projeto do kit. Aí a verificação deixa de ser releitura da peça inteira e vira uma lista curta.

## 6. Você precisa informar o cliente

A Recomendação nº 001/2024 do Conselho Federal da OAB trata do uso ético de IA generativa na advocacia e pede, entre outras coisas: supervisão humana efetiva, veracidade do conteúdo produzido, preservação do sigilo profissional, conformidade com a LGPD, responsabilidade integral do advogado pelo resultado, e **informação ao cliente sobre o uso da tecnologia**.

Esse último item quase ninguém está cumprindo, e é o mais fácil de resolver. Sugestão de cláusula para o contrato de honorários:

> **Uso de ferramentas de inteligência artificial.** O CONTRATADO informa que utiliza ferramentas de inteligência artificial como apoio à pesquisa, organização e redação de documentos, sob supervisão humana integral. Nenhum dado pessoal ou sigiloso do CONTRATANTE é submetido a ferramentas sem tratamento prévio de anonimização. A responsabilidade profissional pelo conteúdo produzido permanece integralmente do CONTRATADO.

Adapte à sua realidade. O ponto é ter a informação registrada. O texto completo, na versão do kit, está em `05-conferencia/clausula_de_ia.md`.

## 7. O risco já se materializou no Brasil

Não é hipótese. Tribunais brasileiros já aplicaram multa por litigância de má-fé por uso de jurisprudência inventada por IA, com ofício à OAB em pelo menos um caso, e o volume de decisões nesse sentido cresceu ao longo de 2025 e 2026. O TJSC tem caso noticiado, e há decisões de fevereiro e março de 2026 na mesma linha.

A defesa "foi a IA que errou" não funciona. A peça tem a sua assinatura e a sua OAB.

Do outro lado do balcão existe regra também: a Resolução CNJ nº 615/2025 regulamenta o uso de IA no Poder Judiciário. O tema não é exótico para quem vai julgar a sua peça.

## Bônus: como ler promessa de ganho de desempenho

Você vai ver números do tipo "com esta configuração a precisão sobe de 85% para 95%". Antes de acreditar, pergunte três coisas: quem avaliou (se foi a própria IA avaliando a própria saída, é autoavaliação, não medição), quantos casos foram testados, e se quem avaliou sabia qual resposta era qual. Testar antes de confiar é a ideia certa. Número sem gabarito externo não é evidência.

## Resumo de bolso

1. Confira a configuração de treinamento e o contrato, não o preço do plano.
2. Aplicação local não é processamento local.
3. Anonimize antes de colar.
4. Nunca peça referência, sempre forneça referência.
5. Quatro partes no prompt, trabalho em etapas.
6. Três passos de verificação antes de protocolar: normas, precedentes, fatos.
7. Informe o cliente por escrito.

E a regra que resume todas: você assina, você responde.
