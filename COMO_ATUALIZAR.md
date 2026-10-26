# Como atualizar a Arvak Library v1.3 para v1.4.0

## 1. Proteja seus dados antes de qualquer alteração

1. No navegador em que você já usa a biblioteca, abra https://danielrosajr.github.io/arvak-library/.
2. Entre em **Dados e backup → Exportar biblioteca**.
3. Salve o JSON em local seguro. Confira se o arquivo não está vazio.
4. **Não limpe dados do navegador**. Não faça upload do backup JSON em repositório público: ele pode conter anotações e links privados do ChatGPT.

## 2. Atualize usando apenas o site do GitHub

1. Acesse https://github.com/danielrosajr/arvak-library.
2. Abra `index.html` (na raiz do repositório).
3. Clique no ícone de **lápis** para editar, ou **Add file → Upload files** para substituir o arquivo com o mesmo nome; confirme que não foi criado um arquivo `index (1).html` e que o `index.html` da raiz foi atualizado.
4. Use o arquivo `index.html` desta entrega para substituir inteiramente o conteúdo antigo. Não envie o `.zip` diretamente como se fosse a aplicação.
5. Clique em **Commit changes** e confirme na branch `main`.
6. Verifique **Settings → Pages → Deploy from a branch → main → /(root)**.
7. Entre em https://danielrosajr.github.io/arvak-library/ e atualize a página (Ctrl+Shift+R, se preciso).

**Commit:** `feat: add project ranking, custom weights and manual priorities`

## 3. Verifique antes de usar

- Seus projetos cadastrados manualmente continuam no catálogo?
- Seus favoritos, links de ChatGPT, bugs, correções e ideias continuam intactos?
- Aparece **Ranking de Projetos** no menu esquerdo?
- Projetos ainda não avaliados exibem “Aguardando avaliação”?
- Você consegue avaliar um projeto, ajustar pesos e mover o ranking manual?
- O filtro e o tema continuam funcionando no celular?

## 4. Se não aparecerem seus projetos

Abra **Dados e backup → Importar backup**, selecione o JSON que baixou, confira a **prévia do número de projetos/ajustes** e confirme a substituição. Isso substitui sua configuração atual. Se você já adicionou dados novos nesta versão, exporte-os primeiro.

A cópia local feita antes da primeira abertura da v1.4 pode ser baixada em **Dados e backup → Cópia antes da v1.4**, se o navegador ainda possuir esse dado. Ela não substitui o backup JSON externo.

## 5. Próximas atualizações

Repita o processo com o `index.html` de cada release, sempre exportando backup antes. Todos os campos conhecidos continuam no mesmo formato de dados (`arvak-library-v1`).
