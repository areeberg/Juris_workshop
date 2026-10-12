# Pseudonimização offline com Gemma 3 4B

Arquivos desta pasta:

- `caso-exemplo.docx`: ficha de atendimento fictícia, com dados pessoais e sensíveis. Todos os dados são inventados.
- `caso-exemplo.md`: o mesmo conteúdo em texto, para colar no chat.
- `prompt-pseudonimizacao.md`: prompt com as definições da LGPD e a tarefa.
- `saida-esperada.md`: resultado de referência, para comparar com o que o modelo gerar.

## Como rodar no LM Studio

1. Carregue o Gemma 3 4B (GGUF) e abra um chat novo. Temperatura 0 a 0,2, contexto de 8192 ou mais.
2. Cole o conteúdo de `prompt-pseudonimizacao.md` numa única mensagem e troque `{{COLE AQUI O TEXTO DO DOCUMENTO}}` pelo conteúdo de `caso-exemplo.md`. O Gemma 3 não tem papel de sistema, então tudo vai na mensagem do usuário.
3. Copie a resposta para um arquivo `.md`.

Para um docx seu, converta antes: `pandoc arquivo.docx -t gfm -o arquivo.md`. Anexar o docx direto no LM Studio ativa a busca por trechos (RAG), e o modelo não vê o documento inteiro.

## Limites

Um modelo de 4B erra: pode deixar passar um dado, trocar o número de um marcador ou mexer no texto. Compare sempre com o original antes de usar a saída fora da máquina. Documentos acima de umas 3 páginas rendem melhor divididos por seção.

A saída é pseudonimizada, mas sem tabela de correspondência não dá para reverter. Se precisar reverter, guarde o mapa marcador/valor à parte, nunca no mesmo arquivo.
