# Guia: texto estruturado (marque onde começa e onde termina cada coisa)

Corresponde aos dois slides "Bom uso de IA" da palestra.

## 1. A ideia

A IA lê de cima para baixo e não sabe, sozinha, onde termina a sua instrução e onde começa o documento que você colou. Quando tudo vem misturado, ela pode tratar um trecho do contrato como ordem, ou esquecer parte da tarefa. Marcadores resolvem.

**Tudo misturado:**

```
Analise o contrato abaixo e liste os riscos para o contratante.
CONTRATO DE PRESTAÇÃO DE SERVIÇOS celebrado entre as partes, que se
obrigam nos termos seguintes, cláusula primeira... responda em tabela
e seja objetivo.
```

**Estruturado:**

```
# TAREFA
Liste os riscos para o contratante.

# CONTRATO
<documento>
...texto colado...
</documento>

# FORMATO
Tabela: cláusula | risco | trecho literal
```

## 2. Que marcador usar

Qualquer um: `#` para títulos, `[ ]` com nome (`[CONTRATO]` ... `[/CONTRATO]`), ou `< >` (`<documento>` ... `</documento>`). O que vale é usar **sempre o mesmo** e **fechar o que abriu**. O formato dos prompts deste kit (`### [PERSONA]`, `### [PROBLEMA]`, `### [PROCESSO]`, `### [PRODUTO]`) é exatamente isso.

## 3. Por que ajuda

1. **Separa a sua instrução do material colado.** A IA sabe o que é ordem e o que é dado.
2. **Ajuda contra instrução escondida.** Se o documento colado trouxer um texto do tipo "ignore as instruções anteriores", a fronteira clara facilita tratá-lo como conteúdo. **Ajuda, não garante.** As instruções do projeto do kit reforçam essa regra, e você continua lendo o resultado.
3. **Evita esquecimento.** Cada parte tem um lugar: tarefa, material, formato.
4. **Você reaproveita.** Prompt com blocos fixos vira modelo.

## 4. Onde guardar o que você escreve

Tenha o seu padrão em arquivo, não na cabeça.

- **Markdown (`.md`).** Texto puro com marcação simples: `# título`, `- lista`, `**negrito**`. Abre em qualquer editor, o Claude lê e escreve nesse formato, e vira Word quando precisar. Todo este kit é feito de arquivos `.md`.
- **Obsidian.** Aplicativo de notas que guarda tudo como arquivos `.md` numa pasta do seu computador, com busca e links entre notas. Serve de biblioteca do escritório: cláusulas, modelos de peça, regras, estilo.
- **Word ou bloco de notas.** Também serve. No Word, use os estilos de título: já é estrutura.

O que não serve é o padrão ficar só na memória de quem redigiu. **Um arquivo por assunto**: é o arquivo que você anexa ao projeto.

Observação sobre confidencialidade: se a sua pasta do Obsidian ficar sincronizada com um serviço na nuvem, o que está nela também sai do computador. Mantenha dados de cliente fora dessa pasta de modelos.

## 5. Um modelo de `.md` para tarefas repetidas

```markdown
# TAREFA
[o que fazer, em uma frase]

# PERSONA
[quem escreve]

# MATERIAL
<documento>
[cole aqui]
</documento>

# PROCESSO
[etapas e onde parar]

# PRODUTO
[formato, tom, proibições]
Cole aqui a regra do Produto: 03-prompts/10_regra_do_produto.md
```
