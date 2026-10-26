# Arvak Library v1.6.0 — Idea Vault

**Uma biblioteca pessoal de aplicativos, mods, automações, projetos e ideias ainda não iniciadas.**

A versão 1.6.0 adiciona o **Cofre de Ideias** à Arvak Library v1.5.0 existente. Não é um aplicativo novo. Todas as áreas anteriores continuam no arquivo único `index.html`: projetos, favoritos, GitHub Discovery, Smart Rank, rankings, links do ChatGPT, bugs, correções, ideias futuras, tutorial e backups.

## ✧ Cofre de Ideias

Selecione **Cofre de Ideias** no menu lateral. A nova área reúne:

- Projetos com status `Ideia` (inclusive antigos, ainda sem prompt).
- Projetos com conteúdo salvo no Cofre, mesmo que depois mudem de status para `Em andamento`, `Pausado` ou outro.
- Contagem de ideias, prompts salvos e ideias prontas para começar.
- Busca por título, descrição, prompt, motivo, resultado desejado e notas.
- Filtros para `Sem prompt`, `Com prompt`, `Prontas para começar` e `Ainda na fase de ideia`.
- Ordenação por edição mais recente ou nome.

Ao criar uma ideia em **Guardar nova ideia**, informe o nome, selecione (automaticamente) o status **Ideia** e salve. O editor do Cofre abre em seguida.

Dentro de **Cofre de Ideias**, cada projeto possui campos independentes:

| Campo | Objetivo | Limite |
|---|---|---|
| Prompt completo | Texto para reutilizar no ChatGPT | 40.000 caracteres |
| Por que tive a ideia | Problema, necessidade ou motivação | 2.500 caracteres |
| Resultado final imaginado | Visão do produto final | 2.500 caracteres |
| Notas e referências | Inspirações, links, riscos, hipóteses | 5.000 caracteres |
| Preparação | Rascunho, Estruturada ou Pronta para começar | — |

O texto é salvo automaticamente com um pequeno intervalo enquanto você digita (também existe **Salvar ideia**). O prompt pode ser copiado, exportado em `.txt` ou preenchido a partir de um `.txt` existente. O editor pergunta antes de substituir um prompt já preenchido por um arquivo importado.

**Importante:** as etapas de preparação não mudam o status real do projeto. Uma ideia pode ficar `Pronta para começar` e continuar com status `Ideia`.

## Privacidade e armazenamento

Tudo funciona localmente, sem conta, chave ou API paga. O conteúdo fica no `localStorage` do navegador com a chave original **`arvak-library-v1`**. A Arvak Library não envia automaticamente seus prompts para o ChatGPT, para o GitHub ou para um backend.

- Os dados não são sincronizados entre computadores ou navegadores.
- Exporte o backup JSON regularmente em **Dados e backup → Exportar biblioteca**.
- Guarde esse JSON com cuidado: ele pode conter ideias pessoais, links de conversas e anotações privadas.
- A primeira abertura da v1.6 preserva também uma cópia local anterior à atualização, disponível em **Dados e backup** enquanto o armazenamento do navegador permitir.
- Se o navegador bloquear o salvamento ou ficar sem espaço, o editor exibirá um aviso; nesse caso copie o texto para um arquivo TXT e resolva o problema de armazenamento antes de continuar.
- Os backups da v1.0–v1.5 continuam compatíveis. **Importar** substitui seus dados atuais e requer confirmação. Faça backup antes da importação.

## Execução e publicação

A aplicação é inteiramente estática e está no arquivo **`index.html`**. Não precisa de npm, build, banco de dados ou GitHub Actions.

Repositório: <https://github.com/danielrosajr/arvak-library>

GitHub Pages: <https://danielrosajr.github.io/arvak-library/>

Para atualizar pelo navegador, consulte [COMO_ATUALIZAR.md](COMO_ATUALIZAR.md).

## Qual a diferença de “Ideias para o futuro”?

A seção **Ideias para o futuro** existente continua como lista de funcionalidades de cada projeto, por exemplo "adicionar modo offline" ao NEXO. **Cofre de Ideias** é para propostas de **projetos inteiros**, incluindo o prompt de criação e o motivo de fazer o aplicativo. Os dados não são mesclados nem substituídos.

## Próximas versões

Veja [ROADMAP.md](ROADMAP.md). A próxima proposta é `v1.7.0 — Project Insights`, com comparação de projetos, gráficos e matriz impacto × esforço.

## Licença

Não foi adicionada licença ao projeto nesta versão.
