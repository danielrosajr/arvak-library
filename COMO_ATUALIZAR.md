# Como atualizar Arvak Library para v1.2.0

## 1. Faça backup ANTES de mexer no GitHub

1. Abra a biblioteca que você já utiliza, no mesmo navegador onde cadastrou seus projetos: https://danielrosajr.github.io/arvak-library/
2. Clique em **Dados e backup** → **Exportar biblioteca**.
3. Guarde o JSON em uma pasta segura, fora do GitHub público.
4. **Não use a função de restaurar biblioteca**, pois ela apaga suas personalizações.

## 2. Atualize sem terminal (site do GitHub)

1. Extraia o arquivo ZIP da v1.2.0 no computador.
2. Abra o repositório: https://github.com/danielrosajr/arvak-library
3. Clique no arquivo `index.html` **na raiz**.
4. Clique no ícone de lápis **Edit this file**.
5. Apague o conteúdo antigo e cole o conteúdo completo do `index.html` que veio no ZIP.
6. Clique em **Commit changes** e confirme que está na branch `main`.
7. Seus ajustes do GitHub Pages continuam os mesmos: **Settings → Pages → Deploy from a branch → main → / (root)**.
8. Abra: https://danielrosajr.github.io/arvak-library/ e atualize a página. Se necessário, use Ctrl+Shift+R para descartar o HTML em cache.

**Atenção:** não faça upload do `.zip` como se fosse o site. O arquivo a publicar é o `index.html` extraído e atualizado.

## 3. Confira seus dados após atualizar

Confira a quantidade total de projetos, os que você mesmo criou, favoritos, notas, datas e marcações de bugs. O sistema continua usando `arvak-library-v1` no localStorage — não mudou a chave nem a versão do esquema.

Se algum dado não aparecer:

1. Confira que está no **mesmo navegador e endereço** de antes.
2. Vá em **Dados e backup → Importar backup** e selecione o JSON exportado.
3. A importação **substitui** as personalizações atuais; exporte o estado atual antes, se houver mudanças novas.

A v1.2 também guardará uma cópia local anterior em **Dados e backup → Cópia antes da v1.2**, quando o navegador permitir armazenamento local. Isso **não substitui** o JSON baixado.

## 4. Como usar os recursos novos

### Vincular sua conversa do ChatGPT

1. Abra uma conversa sua no ChatGPT e copie a URL da barra do navegador (geralmente começa com `https://chatgpt.com/c/`).
2. Na Arvak Library, abra o projeto pelo botão `⋯`.
3. Cole a URL no campo **Conversa do projeto no ChatGPT** e clique em **Salvar alterações**.
4. O cartão passa a exibir **✦ Chat**. O botão do detalhe **✦ ChatGPT** também fica ativo.

Também é possível associar uma conversa enquanto cadastra um projeto novo. URLs válidas são de `chatgpt.com` e `chat.openai.com`.

**Privacidade:** URLs de compartilhamento podem ser acessíveis a terceiros. Links normais para conversas privadas geralmente exigem sua conta. Os links inseridos também aparecem no JSON exportado.

### Em andamento

Abra o projeto → **Situação do projeto** → **Em andamento** → **Salvar alterações**. Projetos anteriormente definidos como **Ativo** aparecem como **Em andamento** automaticamente na interface.

### Próximas correções e ideias futuras

Abra um projeto → digite na caixa **Próximas correções** ou **Ideias para o futuro** → **Adicionar**. Os itens são salvos imediatamente. Marque o checkbox para concluir ou `×` para remover. No menu lateral, abra a visão geral de correções/ideias; você pode marcar itens resolvidos ali ou abrir o projeto correspondente.

### Tutorial

Clique em **❔ Ajuda**, **Tutorial guiado** no menu ou em **Dados e backup → Rever tutorial**. O tutorial aparece automaticamente uma única vez na v1.2 por navegador, e pode ser reaberto quando quiser.

## GitHub — mensagens recomendadas

**Repository description**:

> A personal, Steam-inspired library to manage apps, active development, bugs, future ideas, and ChatGPT project conversations.

**Commit**: `feat: add ChatGPT links, project roadmap and guided tour`

**Tag**: `v1.2.0`

**Release title**: `Arvak Library v1.2.0 — Project Workflow & ChatGPT Links`

**Topics**: `app-library`, `project-tracker`, `personal-dashboard`, `local-first`, `github-pages`, `javascript`, `productivity`, `side-projects`
