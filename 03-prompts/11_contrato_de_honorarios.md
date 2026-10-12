# Prompt: contrato de honorários

**Quando usar.** O cliente descreveu, por áudio, e-mail ou conversa, o que combinou com você, e você precisa da primeira minuta do contrato de honorários.

**O que ele não faz.** Não define o seu percentual, não promete prazo nem resultado e não entrega minuta pronta para assinatura. Entrega a minuta com as lacunas expostas.

**Versão em habilidade:** `04-habilidades/contrato-de-honorarios/`. Na habilidade, a Persona, o Processo e o Produto já estão guardados, e a sua mensagem fica com o Problema.

É a mesma estrutura do `02_contrato_a_partir_de_briefing.md` (etapas 1 a 4), com as trocas abaixo. Cole o relato do cliente entre `<briefing>` e `</briefing>`.

## Etapa 1: leitura do briefing

### [PERSONA]
Atue como advogado especialista em contratos de honorários advocatícios, com vinte anos de prática em escritório de comarca do interior, acostumado a contratos que sobrevivem a discussão com cliente insatisfeito e à leitura do Tribunal de Ética da OAB.

### [PROBLEMA]
Anexei a transcrição do que o cliente me disse. Preciso do contrato de honorários para cliente [pessoa física ou jurídica], ação de [objeto], modalidade [fixo, êxito ou misto]. Use o padrão de cláusulas do escritório que está no projeto.

<briefing>
[cole aqui a transcrição, pseudonimizada]
</briefing>

### [PROCESSO]
Não redija cláusula nesta etapa. Liste em tabela o que o briefing já define e o que falta. Inclua obrigatoriamente: objeto, forma de pagamento, percentual e base de cálculo do êxito, tratamento da sucumbência, despesas processuais, quem pode receber informação do caso e por qual canal, rescisão. Depois, no máximo cinco perguntas objetivas, ordenadas pelo risco de errar sem a resposta.

### [PRODUTO]
Tabela: elemento, o que o briefing diz, trecho literal. Elemento ausente fica como `[LACUNA]`. Não invente percentual. Sinalize com `[ALERTA]` qualquer pedido do cliente que implique prometer prazo ou resultado, porque a advocacia é obrigação de meio. Inclua nas lacunas a cláusula de informação sobre uso de IA, que vem do padrão do escritório.

## Etapas 2 a 4

Use as etapas 2 (esqueleto), 3 (redação cláusula a cláusula) e 4 (rodada de crítica) do prompt `02_contrato_a_partir_de_briefing.md`, mantendo estas duas regras no Produto:

- A cláusula de uso de IA entra no esqueleto, com o texto do padrão do escritório. Modelo em `05-conferencia/clausula_de_ia.md`.
- Nenhum percentual, valor ou prazo sai preenchido sem que você tenha informado.

## Como conferir a saída

Procure primeiro o que a cliente pediu e a minuta silenciou: autorização para falar com terceiro (a filha que acompanha o caso), pagamento só no êxito, quem paga se perder. Depois confira se a minuta prometeu alguma coisa que você não pode prometer. Por fim, resolva todos os colchetes.
