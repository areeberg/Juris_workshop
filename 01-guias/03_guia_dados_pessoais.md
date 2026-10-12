# Guia: dado pessoal, pseudonimização e ZDR

Complementa a regra 2 do guia de sobrevivência. Corresponde aos três slides de Dados da palestra.

## 1. O que é dado pessoal na sua pasta

**Dado pessoal** é a informação que identifica ou pode identificar uma pessoa natural (LGPD, art. 5º, I). Nome, CPF, RG, endereço, telefone, e-mail, placa, número de processo e também o fato raro numa comarca pequena: "o único dentista que perdeu a filha num acidente em maio" identifica sem citar nome.

**Dado pessoal sensível** é o que trata de saúde, origem racial ou étnica, convicção religiosa, opinião política, filiação sindical, vida sexual, dado genético ou biométrico (art. 5º, II). Tem regras mais duras. Laudo médico, atestado e prontuário são o caso mais comum no escritório.

Print do WhatsApp, laudo, CTPS, extrato bancário: tudo isso é dado pessoal. Colar na ferramenta de IA é entregar dado a um **operador** (art. 5º, VII). O escritório é o **controlador** (art. 5º, VI) e responde. O tratamento precisa de finalidade, necessidade e base legal (arts. 6º e 7º).

O sigilo profissional (Estatuto da Advocacia, art. 34, VII) vale mesmo para o dado que a LGPD trata como comum, e vale também para o dado que já está em autos públicos.

## 2. Pseudonimizar não é anonimizar

| | O que é | Continua sendo dado pessoal? |
|---|---|---|
| **Pseudonimização** | Troca o identificador por um código (CLIENTE, LOJA, FILHA) e guarda a tabela de correspondência separada, sob o seu controle | **Sim** (art. 13, §4º) |
| **Anonimização** | Remove ou generaliza até que ninguém consiga reidentificar com esforço razoável | Não (art. 12), mas é mais difícil do que parece |

Na prática, o que o escritório faz é pseudonimizar. Chamar isso de anonimização dá falsa tranquilidade: se a tabela vazar, ou se o fato for raro demais, o dado volta a identificar.

## 3. Quatro boas práticas antes de colar

1. **Offline e antes.** Use localizar e substituir no Word ou no editor, no seu computador. Pedir à própria IA que anonimize o documento é já entregá-lo: o dado saiu no pedido.
2. **Nome vira papel.** CLIENTE, LOJA, FILHA, JUIZ. A tabela de correspondência (papel e nome real) fica em arquivo no seu computador, fora do projeto. Você troca de volta só no arquivo final, no Word, nunca no chat.
3. **Tire o que a tarefa não precisa.** CPF, RG, endereço, telefone, e-mail, placa, número de processo. A pergunta é: a IA precisa disso para fazer esta tarefa? Quase sempre não.
4. **Olhe o indireto.** Em comarca pequena, o fato raro identifica sem nome. Cabeçalho, rodapé, nome de arquivo e metadados do PDF também. Se o caso é inconfundível, pseudonimizar não basta: generalize o fato (ou não use a ferramenta).

Exemplo:

> Antes: "A Sra. Marta Souza, CPF 000.000.000-00, pagou a fatura da Casa Bela em 12/03/2026 e teve o nome negativado em 09/05."
> Depois: "A CLIENTE pagou a fatura da LOJA em 12/03/2026 e teve o nome negativado em 09/05."

### Pseudonimizar com um modelo local

Localizar e substituir funciona bem com poucos nomes. Num documento cheio de dados, um modelo de IA que roda no seu computador, sem internet, faz a primeira passada: nada sai da máquina, então não vale a regra de que pedir à IA já é entregar o documento. Exemplo, prompt e resultado de referência em `06-pseudonimizacao/`. Modelo pequeno erra: confira a saída contra o original antes de usar fora do seu computador.

## 4. ZDR: retenção zero de dados

**O que é.** Acordo contratual em que o fornecedor não guarda as suas entradas e saídas depois de processar, salvo exigência legal ou combate a abuso.

**O que não é.**

- Não é um botão da conta gratuita, Pro ou Max. É um acordo, com aprovação do fornecedor.
- Não é o mesmo que "treino desligado". Com o treino desligado, o fornecedor ainda pode reter as conversas por um período.
- Não dispensa a pseudonimização.

No caso da Anthropic, o ZDR vale para APIs elegíveis (e para o Claude Code em plano Enterprise), mediante acordo e aprovação, e mantém exceções: exigência legal, uso abusivo e classificadores de segurança. Alguns modelos e recursos não são cobertos. **Pergunte ao fornecedor, por escrito, a quais produtos e modelos o ZDR se aplica**, porque a cobertura muda e planos de consumidor não estão incluídos. Confirme na documentação oficial do fornecedor antes de afirmar a um cliente que o dado "não é guardado".

## 5. As camadas, nesta ordem

1. **Não colar o que não precisa.** Elimina o risco na origem.
2. **Pseudonimizar.** Reduz o que sai.
3. **Treino desligado.** Configuração da conta, uma vez só (na palestra: 90 segundos, celular na mão).
4. **Contrato empresarial com ZDR.** Para o escritório que cresce e que trata volume de dado sensível.

Nenhuma camada substitui a anterior.

## 6. Se o incidente acontecer

Dado de cliente colado onde não devia: anote o que saiu, quando e onde. Se houver risco ou dano relevante aos titulares, a LGPD exige comunicar a ANPD e o titular (art. 48), no prazo de três dias úteis (Resolução CD/ANPD nº 15/2024). Procure orientação especializada logo. Esta é uma orientação geral, não parecer sobre o seu caso.

## O que fazer com isto na segunda-feira

Abra o seu modelo de contrato de honorários e acrescente a cláusula de IA (`05-conferencia/clausula_de_ia.md`). Faça a primeira linha do registro de uso (`05-conferencia/registro_de_uso.csv`). Desligue o treino na ferramenta que você usa.
