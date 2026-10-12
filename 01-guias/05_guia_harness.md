# Guia: o harness do escritório

Corresponde ao slide "Onde isso tudo fica guardado".

O modelo é o motor. O **harness** é tudo o que fica em volta dele e o faz trabalhar do seu jeito. Sem harness, você reescreve as mesmas regras em toda conversa.

| Peça | Em uma linha | No kit |
|---|---|---|
| **Projeto** | A pasta da área ou do caso: reúne documentos e regras | Um projeto por área (consumidor, trabalhista...). Contexto misturado piora a resposta |
| **Regras** | Instruções permanentes: o que sempre fazer e o que nunca fazer | `02-projeto/01_instrucoes_do_projeto.md`, no campo de instruções do projeto |
| **Habilidade (skill)** | O prompt de uma tarefa que se repete, guardado: Persona, Processo e Produto | `04-habilidades/` |
| **Memória** | O que a ferramenta lembra entre conversas | Use para preferência, nunca para dado de cliente. Revise o que ela guardou |
| **Contexto do escritório** | Padrão de cláusulas, modelos de peça, áreas, o jeito da casa | `02-projeto/modelo_contexto_do_escritorio.md` |
| **Contexto da pessoa** | O seu estilo de escrever: tom, vocabulário, como você fala com o cliente | `02-projeto/modelo_contexto_da_pessoa.md` |

Sobra para você o **Problema**: o caso concreto e os documentos dele.

## Montagem em quatro passos (uma hora, uma vez)

1. Crie o projeto da área. Cole `01_instrucoes_do_projeto.md` nas instruções.
2. Preencha e anexe o contexto do escritório. Só o que você tem certeza de que é regra da casa.
3. Faça e anexe o contexto da pessoa, com três textos seus pseudonimizados.
4. Instale as habilidades que você leu inteiras (`04-habilidades/COMO_CRIAR.md`). Sem plano pago, deixe os prompts de `03-prompts/` à mão.

## Os limites

- **Plano.** Habilidades próprias exigem plano pago. O projeto e as instruções dependem do plano e da ferramenta: confira na sua.
- **Versão.** Habilidades e instruções do projeto podem não manter histórico que você consiga consultar. Guarde cópia datada em arquivo seu. Os documentos que o Claude cria na conversa guardam as versões anteriores, e cada rodada de crítica é uma versão.
- **Conector.** É o cabo para um sistema externo (tribunal, e-mail, agenda). Fica fora do harness básico. Veja `02_guia_conexao_fontes_publicas.md`, depois de consolidar o básico.
- **Memória e sigilo.** Se a ferramenta lembra entre conversas, o que você contou pode reaparecer em outra. Não conte dado de cliente.
- **O harness não faz a conferência.** Ele reduz o retrabalho. Quem lê, confere e assina é você.
