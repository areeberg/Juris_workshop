# Prompts do escritório, formato 4 Ps

Todos os prompts seguem a mesma estrutura, os 4 Ps, e têm duas coisas em comum: o trabalho em etapas, com parada para conferência, e a seção final "como conferir a saída".

Cada arquivo é um prompt pronto para colar. A ideia não é decorar os prompts, é decorar o esqueleto: com ele você escreve o seu próprio prompt para qualquer tarefa, em qualquer ferramenta.

## O esqueleto

**Persona.** Quem está escrevendo. Sem isso a IA assume a média da internet. Diga a especialidade, os anos de experiência e o padrão de exigência de quem vai revisar o texto.

**Problema.** Qual resultado jurídico prático você quer. Não é "escrever um texto", é "demonstrar a improcedência" ou "entregar uma minuta que sobreviva a litígio". Aqui também entra o que usar e o que ignorar do que já foi conversado.

**Processo.** Como o trabalho deve ser executado. Quase sempre: primeiro o esqueleto para você validar, depois cada parte separadamente. Nunca a peça inteira de uma vez.

**Produto.** Formato, tamanho, tom e proibições. É a parte que impede a alucinação, e é a que a maioria esquece.

## A regra que não pode faltar

Todo prompt jurídico deve proibir, no Produto, citação de jurisprudência, súmula, enunciado ou doutrina que não tenha sido colada por você. A folha `10_regra_do_produto.md` (nesta pasta) traz esse bloco pronto para colar em qualquer prompt, inclusive nos que não estão neste kit.

## Ordem de uso

1. `02-projeto/01_instrucoes_do_projeto.md` vai uma vez só, nas instruções do projeto. Vale para todas as conversas daquele projeto e é o que sustenta as marcações usadas em todos os prompts.
2. Os prompts de 02 a 08 e o 11 vão na conversa, um por tarefa. O 11 (contrato de honorários) é a variação do 02 usada na palestra.
3. `09_checklist_pre_protocolo.md` é folha impressa, não é prompt.
4. Tarefa que você repete toda semana vira **habilidade** (`04-habilidades/`). O prompt continua valendo para quem não tem plano pago.

Crie um projeto por área (cível, previdenciário, trabalhista). Contexto misturado piora a resposta.

## As marcações usadas em todo o kit

| Marcação | Significa |
|---|---|
| `[VERIFICAR]` | Citação normativa que precisa ser conferida na fonte oficial |
| `[INSERIR JULGADO AQUI]` | Lugar onde entra precedente que você vai pesquisar |
| `[FATO A CONFIRMAR: ...]` | Fato que a peça pressupõe e o material não comprova |
| `[LACUNA: ...]` | Informação que falta para completar a tarefa |
| `[FALTA PRECEDENTE: ...]` | Argumento que só fecha com julgado que você ainda não tem |
| `[CONFERIR PRAZO]` | Prazo que saiu do documento e precisa da sua validação |
| `[ALERTA]` | Pedido do cliente que implica prometer prazo ou resultado (obrigação de meio) |
| `[RISCO]` | Cláusula que protege de um risco específico, dito na marcação |

Nenhum documento sai do escritório com colchete não resolvido.

## Antes de rodar qualquer prompt

Pseudonimize (nome vira papel, tabela de correspondência fora do projeto), retire CPF, CNPJ, endereço e número de processo em segredo de justiça, e delimite o que você cola com marcas como `<documento>`. Veja `01-guias/03_guia_dados_pessoais.md` e `04_guia_texto_estruturado.md`. Confira a política de dados e a configuração de treinamento da ferramenta que você usa. Aplicação instalada na máquina não significa processamento na máquina: o conteúdo é enviado ao servidor do fornecedor de qualquer forma.

## O que este kit não faz

Não dispensa a conferência. A responsabilidade pela peça é integralmente sua, e a Recomendação OAB 001/2024 exige supervisão humana efetiva, veracidade, preservação do sigilo e informação ao cliente sobre o uso de IA.
