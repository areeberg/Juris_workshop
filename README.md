# IA no trabalho jurídico: material da palestra

Material de apoio da palestra **"IA no trabalho jurídico: como fazer um uso eficiente da IA"**, apresentada à OAB, 16ª Subseção de Juína/MT, por Alexandre Reeberg de Mello. É para quem advoga e quer usar IA com método: sem citação inventada, sem quebrar o sigilo e sem entregar a assinatura para a máquina.

> Você assina, você responde. Este material é método de trabalho, não parecer jurídico.

## Sobre o treinamento

Foram 60 minutos de apresentação e 30 de conversa. A palestra segue um caso fictício, o da Dona Marta: ela pagou uma fatura em março e teve o nome negativado em maio. Da cliente chegam um áudio e uma pasta de documentos. A partir daí, cada bloco resolve uma etapa do trabalho com IA.

| Bloco | O que você leva |
|---|---|
| Abertura | O caso real que virou multa e a regra: quem assina, responde |
| Como ela funciona | Seis intuições sobre o modelo e como escrever para ele (texto estruturado) |
| Contrato | Do áudio da cliente ao contrato de honorários, com os quatro Ps |
| Acervo | A cronologia dos fatos, com página de origem para cada linha |
| Advogado do diabo | Por onde a sua peça cai, antes da parte contrária |
| Citações | Pesquisa sem multa: você pesquisa na fonte, a IA costura |
| Ética, LGPD e dados | Sigilo, dado pessoal, pseudonimização, treino desligado e ZDR |
| Fechamento | O que fazer com o tempo que sobra e o que fazer na segunda-feira |

Quatro ideias sustentam o resto:

1. A IA prevê a continuação mais provável do texto. Ela erra por fluência, não por ignorância, e a segurança do tom não diz nada sobre estar certa.
2. Todo o método é um movimento só: passar as coisas da memória da IA para a mesa. Nunca peça referência, sempre forneça.
3. Pseudonimizar não é anonimizar. O dado continua sendo pessoal, e quem responde é o escritório.
4. Nenhum documento sai com colchete aberto: `[VERIFICAR]`, `[LACUNA]`, `[FATO A CONFIRMAR]` e as outras marcas são trabalho seu, não da IA.

## O que tem aqui

| Pasta | Conteúdo |
|---|---|
| `apresentacao/` | Os slides da palestra em PDF |
| `00-comece-aqui/` | Mapa da palestra para o kit e a folha de segunda-feira |
| `01-guias/` | Sobrevivência (sete regras), fontes públicas, dados pessoais e ZDR, texto estruturado, harness |
| `02-projeto/` | Instruções do projeto e modelos de contexto do escritório e da pessoa |
| `03-prompts/` | Prompts dos quatro Ps: contrato, cronologia, peça, red team, pesquisa, triagem, tradução ao cliente, checklist, regra do Produto |
| `04-habilidades/` | Três habilidades prontas para o Claude (`SKILL.md` e `.zip`) e como instalar |
| `05-conferencia/` | Seis perguntas de risco, matriz de risco, pode ou não pode, cláusula de IA, registro de uso |
| `06-pseudonimizacao/` | Demonstração da palestra: documento fictício, prompt e resultado de referência para pseudonimizar offline |
| `caso-ficticio-dona-marta/` | O caso inventado da palestra, com áudio transcrito, dossiê, petição e súmulas, para você treinar |

Os slides marcados como "Clipe" eram vídeos curtos na palestra. No PDF aparece um quadro de cada. Você reproduz o mesmo no caso fictício, com as habilidades e os prompts do kit.

## Por onde começar

**Se você tem uma hora:** leia `01-guias/01_guia_sobrevivencia.md`, `03-prompts/10_regra_do_produto.md` e `03-prompts/09_checklist_pre_protocolo.md`.

**Se você tem uma semana:** siga `00-comece-aqui/segunda_feira.md`. São vinte minutos por dia, sempre em caso real, começando por um projeto com as instruções do kit.

**Se quer praticar antes de usar em caso real:** crie um projeto no Claude, cole `02-projeto/01_instrucoes_do_projeto.md` e rode as tarefas no `caso-ficticio-dona-marta/`.

## Habilidades

Em `04-habilidades/zips/`: `contrato-de-honorarios`, `acervo-para-cronologia` e `advogado-do-diabo`. Exigem plano pago do Claude (Pro, Max, Team ou Enterprise). No plano gratuito, cole o conteúdo dos prompts de `03-prompts/`. Instalação e cuidados em `04-habilidades/COMO_CRIAR.md`. **As habilidades ainda não foram testadas em casos reais.**

## Pseudonimizar com um modelo local

A pasta `06-pseudonimizacao/` mostra o que foi feito ao vivo: um modelo pequeno (Gemma 3 4B, quantizado, no LM Studio) troca nomes, CPF, endereço e dados sensíveis por marcadores, sem internet. Tem o documento fictício em `.docx`, o prompt com as definições da LGPD, o resultado de referência e o passo a passo. Modelo pequeno erra: confira a saída contra o original.

## Cuidados

- Pseudonimize antes de colar. Desligue o treino. Entenda o ZDR (`01-guias/03_guia_dados_pessoais.md`).
- Nenhuma citação jurídica sai da IA: você pesquisa na fonte oficial e cola.
- Nenhum documento sai com colchete aberto.
- Tudo o que está em `caso-ficticio-dona-marta/` e `06-pseudonimizacao/` é inventado. Pessoas, loja, números e valores não existem.
- Confira as normas citadas na fonte oficial. A responsabilidade pela peça é de quem assina.

## Licença e créditos

Uso profissional pessoal, sem revenda, redistribuição ou treinamento de modelos. Veja `LICENCA.md`. As folhas de risco adaptam o trabalho de Graziela Bonfim, da Comissão de IA da OAB/RJ.

Autor: Alexandre Reeberg de Mello.
