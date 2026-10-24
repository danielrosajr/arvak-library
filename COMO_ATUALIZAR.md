# Como atualizar para Arvak Library v1.3.0

## 1 — Faça backup ANTES de publicar

Abra sua biblioteca atual **no mesmo navegador onde cadastrou seus projetos**:

https://danielrosajr.github.io/arvak-library/

Use **Dados e backup → Exportar biblioteca**. Guarde o `.json` gerado em local seguro. Ele contém seus projetos adicionados, anotações, links do ChatGPT e outras personalizações, portanto **não faça upload público desse arquivo**.

**Por que é importante?** Todos os seus projetos personalizados ficam no navegador, não no repositório GitHub. Atualizar o HTML no mesmo domínio normalmente preserva tudo, mas usar outro navegador/dispositivo, navegar em modo anônimo ou limpar dados do site pode apresentar biblioteca vazia.

## 2 — Atualize pelo GitHub, sem terminal

1. Extraia o ZIP v1.3.0.
2. Entre em https://github.com/danielrosajr/arvak-library
3. Na raiz, abra **`index.html`**.
4. Clique no lápis **Edit this file** e substitua o conteúdo pelo conteúdo integral do `index.html` da v1.3.0.
5. Clique em **Commit changes** na branch `main`.
6. Abra **Settings → Pages** e mantenha a origem **Deploy from a branch** (`main` e `/(root)`). Não precisa de GitHub Actions nem npm.
7. Abra https://danielrosajr.github.io/arvak-library/ e atualize a página, se necessário com Ctrl+Shift+R.

Também pode usar **Add file → Upload files** para enviar `index.html`, mas confira se o GitHub realmente substituiu o arquivo existente. NÃO envie o ZIP como um único arquivo.

## 3 — Experimente a descoberta

1. Clique **Buscar projetos** (acima) ou **Descobrir no GitHub** (menu lateral).
2. Clique **Escanear GitHub** para consultar a lista atual.
3. Em cada sugestão, escolha **Adicionar à biblioteca** ou **Ignorar sugestão**.
4. Se o repositório tem GitHub Pages, marque a opção do URL padrão somente quando fizer sentido. Confirme depois que abre.
5. Depois de adicionar, clique em `⋯` no cartão para escolher o status real, anotar correções, ideias e link do ChatGPT.
6. Para rever sugestões ignoradas, marque **Mostrar ignorados**.
7. Em **Dados e backup**, desative **Busca automática do GitHub** se quiser verificar só manualmente.

## 4 — Seus dados antigos

A chave permanece `arvak-library-v1`, e a estrutura de dados é compatível com versões 1.0–1.2. O site cria uma cópia local anterior à primeira abertura da v1.3. Você pode baixá-la em **Dados e backup → Cópia antes da v1.3**.

Se algo não aparecer, importe seu JSON anterior usando **Dados e backup → Importar backup**. Atenção: a importação substitui as personalizações atuais; exporte um backup novo primeiro, se necessário.

## Informações sugeridas para o GitHub

- **Repository name:** `arvak-library`
- **Description:** `A personal, Steam-inspired app library with GitHub project discovery, progress tracking, bug lists, and quick links to apps and ChatGPT conversations.`
- **Topics:** `app-library`, `project-tracker`, `github-api`, `github-pages`, `javascript`, `local-first`, `productivity`, `side-projects`
- **Version / Tag:** `v1.3.0`
- **Commit message:** `feat: discover new GitHub repositories and suggest projects`
- **Release title:** `Arvak Library v1.3.0 — GitHub Project Discovery`

Veja `RELEASE_NOTES.md` para o texto completo da release.
