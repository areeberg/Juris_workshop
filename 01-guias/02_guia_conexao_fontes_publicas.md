# Guia avançado: conectando a IA a fontes públicas

**Leia isto depois do evento, com calma, no seu computador.** Este guia não faz parte da palestra. Ele exige instalação de software, edição de arquivo de configuração e, para a parte jurídica, uma chave de API do CNJ. Nada disso cabe em 60 minutos de palestra.

**Antes de começar, calibre a expectativa.** Os dois servidores descritos aqui são projetos abertos, mantidos por voluntários, em estágios diferentes de maturidade. O fiscal está em beta e funciona bem. O jurídico está em versão 0.1, classificada como pré-alfa pelo próprio autor. Trate como ferramenta de exploração, não como sistema do qual o seu prazo depende.

---

**Atualização de setembro de 2026.** Três avisos antes de qualquer coisa neste guia.

Primeiro: conectar a IA a uma fonte externa não a torna confiável. Ela passa a receber dado real de onde a conexão alcança, e continua produzindo texto provável em tudo o que estiver fora dali.

Segundo: instalar um servidor no seu computador não faz o processamento acontecer no seu computador. O servidor busca o dado localmente e o conteúdo continua sendo enviado ao fornecedor do modelo para ser interpretado. Vale a regra 1 do guia de sobrevivência.

Terceiro: não encadeie uma IA em outra. Mandar a ferramenta navegar até outro site de IA, colher a resposta e transformar em peça são duas gerações sem conferência humana no meio, com dados do caso saindo para um terceiro sem contrato com o escritório.

---

## 1. O que é MCP

O Model Context Protocol permite que uma IA use ferramentas externas em vez de depender só do que você cola no chat. Em vez de você abrir o site, copiar e colar, a própria IA consulta a fonte e traz o resultado estruturado.

Na prática: você pede em português, e nos bastidores a IA aciona uma função como `buscar_processo_por_numero` ou `consultar_cnpj`.

---

## 2. Pré-requisitos

1. **Claude Desktop instalado** (o navegador não serve para servidores locais).
2. **`uv` instalado**, que é o gerenciador de pacotes Python usado para rodar os servidores.
   - Windows (PowerShell): `powershell -c "irm https://astral.sh/uv/install.ps1 | iex"`
   - macOS e Linux: `curl -LsSf https://astral.sh/uv/install.sh | sh`
3. **Permissão de instalação na máquina.** Notebook corporativo com bloqueio de administrador normalmente impede este passo. Se for o seu caso, pare aqui e fale com o TI.
4. **Chave de API do DataJud**, só para o servidor jurídico. Solicite em `datajud-wiki.cnj.jus.br/api-publica/acesso/`.

---

## 3. Configuração

Abra o arquivo de configuração do Claude Desktop:

- Windows: `%APPDATA%\Claude\claude_desktop_config.json`
- macOS: `~/Library/Application Support/Claude/claude_desktop_config.json`

Se o arquivo não existir, crie. Cole o conteúdo abaixo, substituindo `sua-chave-aqui` pela chave que o CNJ enviou:

```json
{
  "mcpServers": {
    "fiscal-brasil": {
      "command": "uvx",
      "args": ["mcp-fiscal-brasil"]
    },
    "juridico-brasil": {
      "command": "uvx",
      "args": ["mcp-juridico-brasil"],
      "env": {
        "DATAJUD_API_KEY": "sua-chave-aqui"
      }
    }
  }
}
```

**Atenção:** sem o bloco `env` com a chave, todas as consultas de processo do servidor jurídico falham. Essa é a causa número um de "instalei e não funciona".

Salve e **reinicie o Claude Desktop**. Um ícone de ferramentas aparece na barra de digitação quando deu certo.

---

## 4. MCP Fiscal Brasil

O mais maduro dos dois. Não exige chave de API. Cobre CNPJ, NF-e, NFS-e, SPED, eSocial, Simples Nacional, tabelas NCM e CFOP, indexadores do Banco Central e a Reforma Tributária (IBS e CBS).

**Pedidos que funcionam bem:**

- *"Analise o CNPJ [número]. Monte um relatório de due diligence para eu avaliar o risco de contratar essa empresa como fornecedora."*
- *"Valide a estrutura desta chave de acesso de NF-e: [chave]. Aponte inconsistências."*
- *"Compare Lucro Presumido e Simples Nacional para uma prestadora de serviços faturando 500 mil por ano."*

**Onde ele é útil na advocacia:** direito empresarial, contratos, due diligence de fornecedor e de parte contrária, tributário, e verificação de saúde financeira de reclamada em trabalhista.

---

## 5. MCP Jurídico Brasil, e o que ele não faz

Conecta ao DataJud do CNJ, que cobre 91 tribunais. Ferramentas disponíveis: busca de processo por número, listagem de movimentações, resumo de andamento, monitoramento com snapshot, cálculo de prazo em dias úteis e listagem de tribunais.

**Leia esta caixa antes de confiar nele em qualquer coisa:**

> **Limitações do DataJud.** A API pública traz metadados: cabeçalho do processo e códigos padronizados de movimentação.
> - **Não traz** partes nem advogados.
> - **Não traz** o teor de decisões, despachos ou sentenças.
> - **Não traz** publicações e intimações.
> - **Não permite** busca por CPF ou CNPJ.
> - **Não retorna** processos em segredo de justiça.
>
> **Consequência prática mais importante: não use para controle de prazo.** Prazo processual corre da intimação, que vem do Diário de Justiça Eletrônico Nacional e do Domicílio Judicial Eletrônico, e a intimação não está no DataJud. O cálculo em dias úteis que a ferramenta faz está correto como aritmética do CPC, mas a **data inicial** que você vai informar não pode vir do DataJud. Continue usando o seu sistema de controle de prazos.
>
> **Sobre monitoramento:** a ferramenta de monitorar processo guarda um retrato na memória da sessão e compara quando você pede de novo. Ela não avisa sozinha. Alerta automático e webhook estão no roteiro futuro do projeto, não na versão atual.

**Pedidos que funcionam:**

- *"Busque o processo [número no formato CNJ] e liste as movimentações desde março."*
- *"Quais tribunais estão disponíveis para consulta?"*
- *"Considerando que a intimação ocorreu em 15/05, calcule o prazo final de 15 dias úteis para contestação, aplicando o calendário forense."* (note: a data de intimação vem de você, não da ferramenta)

**Pedidos que vão frustrar:**

- "Quem é o advogado da parte contrária nesse processo?"
- "Me mostre o teor da sentença."
- "Busque todos os processos do CPF tal."
- "Monitore e me avise quando mexer."

---

## 6. Combinando com Projects

O ganho real aparece quando você junta as duas coisas: um Project do Claude com os documentos do caso (anonimizados) e as instruções de redação do escritório, mais os servidores MCP conectados. Aí a IA tem os fatos do seu caso e a capacidade de consultar situação fiscal e andamento processual na mesma conversa.

---

## 7. Se algo der errado

| Sintoma | Causa mais provável |
|---|---|
| Ícone de ferramentas não aparece | JSON com erro de sintaxe, ou Claude Desktop não reiniciado |
| "Erro de autenticação" no jurídico | Falta o bloco `env` com `DATAJUD_API_KEY` |
| `uvx` não encontrado | `uv` não instalado, ou terminal não reiniciado após instalar |
| Instalação bloqueada | Notebook corporativo sem permissão de administrador |
| Consulta de processo vem vazia | Número fora do formato CNJ, tribunal não coberto, ou processo em segredo de justiça |

---

## 8. Fontes

- mcp-fiscal-brasil: `github.com/DeHor-Labs/mcp-fiscal-brasil`
- mcp-juridico-brasil: `github.com/DeHor-Labs/mcp-juridico-brasil`
- Documentação da API pública do DataJud: `datajud-wiki.cnj.jus.br`
- Especificação do MCP: `modelcontextprotocol.io`
