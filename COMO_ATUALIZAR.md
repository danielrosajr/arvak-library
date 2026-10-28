# Atualização segura da Arvak Library v1.6 → v1.7.0 (sem terminal)

## 1. Backup antes de qualquer alteração

1. Abra `https://danielrosajr.github.io/arvak-library/` no **mesmo navegador** em que você cadastra seus projetos.
2. Clique em **Dados e backup → Exportar biblioteca**.
3. Guarde o JSON em uma pasta fora do navegador (por exemplo Downloads/Backups). Confira que o arquivo existe.
4. **Não** use a opção Restaurar biblioteca inicial.

> Apenas substituir o HTML do GitHub **não apaga** localStorage no mesmo domínio e navegador. Mas uma mudança de navegador, modo anônimo, limpeza de dados ou alteração da origem pode ocultar seus projetos. Por isso o JSON é indispensável.

## 2. Substituir só um arquivo pelo GitHub

1. Abra `https://github.com/danielrosajr/arvak-library`.
2. Na branch `main`, abra o arquivo **`index.html`** da raiz.
3. Clique no ícone de lápis (**Edit this file**).
4. Substitua **todo** o conteúdo pelo novo `index.html` desta entrega. Se preferir, use o upload pelo site do GitHub mantendo o mesmo caminho e confira que o arquivo foi substituído.
5. Em **Commit changes**, use:
   `feat: add Project Insights and pairwise manual ranking`
6. Confirme o commit na branch `main`.
7. Mantenha a publicação do GitHub Pages em **Settings → Pages → Deploy from a branch → main → /(root)**, como já funciona hoje.
8. Abra o site publicado, atualize com Ctrl+Shift+R e confira no topo **v1.7**.

Os arquivos de documentação são opcionais para o funcionamento do site; o `index.html` é suficiente. Não envie o ZIP inteiro como um arquivo único dentro do repositório.

## 3. Confirmar que nenhum dado sumiu

- Confira a quantidade de projetos, favoritos, seus links de ChatGPT, bugs, ideias e correções.
- Abra **Cofre de Ideias**, confira um prompt.
- Abra **Ranking**, confira a ordem manual e as avaliações existentes.
- Vá a **Project Insights**: se você não avaliou critérios suficientes, ver mensagens de "Não avaliado" é normal.
- Faça um novo backup JSON quando terminar de organizar a biblioteca.

## 4. Se estiver tudo vazio

1. **Não clique em Restaurar biblioteca inicial.**
2. Verifique que é o mesmo navegador e endereço (origem) de antes.
3. Em **Dados e backup → Importar backup**, selecione o arquivo JSON exportado no passo 1.
4. Leia a prévia e confirme somente se desejar substituir a coleção atual.
5. Confira os dados restaurados e exporte um novo backup.

O aplicativo também disponibiliza uma **Cópia antes da v1.7** na tela de backups, se existia armazenamento disponível quando a atualização começou. Essa cópia local **não** substitui o backup baixado.

## 5. Versão e release

- **Tag:** `v1.7.0`
- **Título:** `Arvak Library v1.7.0 — Project Insights & Priority Duel`
- **Commit:** `feat: add Project Insights and pairwise manual ranking`
- **Descrição do repositório:** `A personal project library with AI-assisted rankings, pairwise prioritization, impact-effort insights, idea vaults, and GitHub discovery.`
- **Topics:** `project-management`, `app-library`, `project-ranking`, `decision-making`, `pairwise-comparison`, `github-pages`, `local-first`, `javascript`

O arquivo `RELEASE_NOTES.md` contém o texto da release pronto para copiar.
