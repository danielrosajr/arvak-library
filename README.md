# Arvak Library v1.2.0

> Biblioteca pessoal de aplicativos, mods, ferramentas e ideias — organizada como uma pequena estante de jogos.

**Aplicativo estático, em um único `index.html`, sem npm, backend, conta ou banco de dados.**

## O que há de novo

- **Conversa do ChatGPT por projeto:** campo editável nos detalhes (e ao cadastrar projetos) e atalho `✦ Chat` no cartão depois de salvar.
- **Em andamento:** situação específica para projetos sendo desenvolvidos agora. O valor `Ativo` dos dados antigos continua reconhecido e aparece como **Em andamento** na interface.
- **Próximas correções:** checklist individual por projeto, com marcar como resolvido, excluir, pendências e painel geral.
- **Ideias para o futuro:** checklist separado de correções com visão geral por projeto.
- **Mini tutorial guiado:** seis passos, abre na primeira visita desta versão e pode ser repetido pelo menu ou Ajuda.
- **Backups:** exportação/importação JSON abrangendo links do ChatGPT, tarefas e todo o histórico já existente. Cópia local automática dos dados disponíveis antes da v1.2, mantendo a cópia anterior da v1.1.

## Estados disponíveis

`A organizar` · `Em andamento` · `Pausado` · `Em testes` · `Concluído` · `Ideia` · `Arquivado`.

**Com bug** é uma marcação independente, podendo coexistir com qualquer um dos estados. O campo livre de bugs da v1.1 permanece preservado. Os itens em **Próximas correções** são tarefas extras, não substituem as notas antigas.

## Dados e privacidade

- Os dados ficam no **localStorage** deste navegador, na mesma chave anterior: `arvak-library-v1`.
- Atualizar o `index.html` **no mesmo endereço e navegador** não apaga seus projetos personalizados por si só.
- Se trocar navegador, dispositivo, domínio, limpar dados do site ou usar janela anônima, seus dados podem não aparecer.
- Sempre **exporte o JSON antes de atualizar**. Salve-o em local privado e seguro.
- Os URLs de conversas do ChatGPT são privados por padrão somente enquanto forem dados locais. **Links de compartilhamento do ChatGPT podem permitir leitura por qualquer pessoa com o link**, e todos os links inseridos constam também no JSON de backup. Não publique esse JSON em repositórios públicos.
- Abrir uma conversa normal pode exigir estar logado no ChatGPT e ter acesso à conversa.
- Não há sincronização automática nem acesso à API do ChatGPT.
- A consulta opcional de datas de push busca somente metadados públicos na API do GitHub.

## Publicação / atualização

Consulte [COMO_ATUALIZAR.md](COMO_ATUALIZAR.md). O projeto funciona em GitHub Pages **Deploy from a branch**, com o `index.html` na raiz e sem build.

## Testes feitos

- JavaScript analisado com `node --check` (Node 22).
- Chromium/Playwright: adicionar projeto, registrar link de conversa, alterar estado, criar/marcar correções, cadastrar ideias, filtrar itens e persistir em armazenamento simulado.
- Compatibilidade com dados da v1.1: projeto manual, notas, favorito e marcação de bugs preservados.
- Exportação e importação JSON da v1.2 com itens e conversa; importação de um backup v1.1.
- Testes funcionais em largura mobile (390px). O carregamento do HTML foi simulado no navegador com `set_content` porque o ambiente bloqueou navegação local por política; deploy público ainda deve ser conferido no seu GitHub Pages.

## Repositório sugerido

- **Repository:** `arvak-library`
- **Description:** `A personal, Steam-inspired library to manage apps, active development, bugs, future ideas, and ChatGPT project conversations.`
- **Topics:** `app-library`, `project-tracker`, `personal-dashboard`, `local-first`, `github-pages`, `javascript`, `productivity`, `side-projects`
- **Tag:** `v1.2.0`
- **Commit:** `feat: add ChatGPT links, project roadmap and guided tour`
- **Release:** `Arvak Library v1.2.0 — Project Workflow & ChatGPT Links`
