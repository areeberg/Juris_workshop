# Como usar as três habilidades

Habilidade (skill) é o prompt de uma tarefa que se repete, guardado em uma pasta, com nome e descrição. O Claude lê a descrição e decide sozinho quando usá-la; você também pode pedir pelo nome ("Use a habilidade contrato-de-honorarios"). Não existe comando de barra para chamá-la no claude.ai.

## Antes de tudo

- **Plano.** Habilidades próprias exigem plano pago (Pro, Max, Team ou Enterprise). No plano gratuito, cole o prompt equivalente de `03-prompts/` na conversa. O resultado é o mesmo, com mais colagem.
- **Teste.** As três habilidades deste kit foram escritas a partir dos prompts do kit e **ainda não foram testadas em casos reais**. Rode primeiro no caso fictício (`caso-ficticio-dona-marta/`) e leia o que sai antes de usar em caso de cliente.
- **Confira os passos na sua tela.** O caminho dos menus muda. O que está abaixo foi verificado na documentação em outubro de 2026.

## Instalar

1. Em `zips/`, escolha o arquivo `.zip` da habilidade. Cada zip contém uma pasta com o mesmo nome da habilidade e, dentro, o `SKILL.md`.
2. No Claude, abra **Configurações > Capacidades > Habilidades** e use a opção de enviar uma habilidade, escolhendo o zip. Ative a habilidade.
3. Abra o projeto do caso e peça: "Use a habilidade contrato-de-honorarios." junto com o seu Problema (o caso e os documentos).

## Regras de segurança

- **Instale só habilidade que você leu inteira.** Habilidade é instrução que o Claude segue. Uma habilidade de desconhecido pode trazer instrução escondida (por exemplo, para enviar o conteúdo a terceiros). Se vier de grupo ou rede social, leia o `SKILL.md` por inteiro ou escreva a sua.
- **Habilidade não guarda dado de cliente.** Ela guarda o método. O caso entra na conversa, pseudonimizado.
- **Versione por conta própria.** Habilidades e instruções de projeto não mostram histórico de versões que você possa confiar. Guarde cópia datada: `contrato-de-honorarios_2026-10.md`. Os documentos que o Claude cria na conversa, esses sim, guardam as versões anteriores.

## Criar a sua própria

Peça ao Claude que entreviste você: "Quero criar uma habilidade para [tarefa]. Entreviste-me, uma pergunta por vez, sobre as minhas regras: o que sempre faço, o que nunca entra, o formato de saída." Revise o `SKILL.md` que ele gerar, corte o que não é seu e teste em caso fictício.

## Estrutura mínima de um SKILL.md

```markdown
---
name: nome-em-minusculas-com-hifen
description: O que faz e quando usar, em uma ou duas frases. É a descrição que faz o Claude escolher a habilidade.
---

# Título

Persona. Processo (etapas, com paradas). Produto (formato e proibições).
```

O `Problema` não entra na habilidade: é o caso concreto e muda a cada uso.
