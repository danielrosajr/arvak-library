# Como atualizar sua Arvak Library para a v1.1.0 sem perder projetos

## ETAPA 1 — Backup OBRIGATÓRIO recomendado

1. Use o **mesmo dispositivo e o mesmo navegador** onde você já criou projetos.
2. Entre na **versão atual** da biblioteca: https://danielrosajr.github.io/arvak-library/
3. Clique em **Dados e backup** no menu lateral.
4. Clique em **Exportar biblioteca**.
5. Confirme que um arquivo parecido com `arvak-library-backup-2026-10-23.json` foi salvo em Downloads.
6. Guarde esse arquivo fora do navegador. **Não envie esse JSON para o GitHub público**: ele pode incluir suas notas pessoais.

Esse passo é essencial: quando você cria um projeto, ele **não** é salvo no código do GitHub; ele fica no armazenamento local do navegador (`localStorage`).

## ETAPA 2 — Atualize o projeto pelo próprio GitHub (sem comandos)

1. Extraia o ZIP `Arvak-Library-v1.1.0.zip` no computador.
2. Acesse https://github.com/danielrosajr/arvak-library
3. Atualize o arquivo **`index.html` na raiz** com o `index.html` desta versão. Você pode abrir o arquivo no GitHub, clicar no lápis (Edit this file), substituir o conteúdo inteiro e confirmar o commit. Alternativamente, use **Add file → Upload files** se a interface permitir substituir o arquivo existente.
4. Não crie subpastas extras: o arquivo precisa ficar em `/index.html`, não em `/arvak-library-v1.1.0/index.html`.
5. Aguarde a publicação terminar no GitHub Pages (ou confira a aba Actions, se usar publicação automatizada).
6. Abra https://danielrosajr.github.io/arvak-library/ e recarregue a página.

## ETAPA 3 — Confira seus dados

Confira se aparecem seus projetos pessoais, favoritos, anotações e situações anteriores. Na v1.1 há novos filtros **Em testes** e **Com bug**, e campos de problema ao abrir os detalhes de um projeto.

### Se estiver tudo certo

Continue usando normalmente. Sempre que fizer muitas alterações, exporte um novo backup JSON.

### Se seus projetos pessoais não aparecerem

1. **Não pressione Restaurar biblioteca inicial.**
2. Confira se você está no navegador e domínio em que os cadastrou. Um arquivo HTML aberto localmente usa armazenamento diferente do site no GitHub Pages.
3. Abra **Dados e backup → Importar backup** e escolha o JSON que salvou na ETAPA 1. A importação **substitui** os dados deste navegador; exporte primeiro quaisquer dados mais novos que queira preservar.
4. Se você não tiver o JSON, volte ao navegador/endereço original e exporte a biblioteca de lá, desde que os dados ainda estejam armazenados.

### Cópia automática de segurança da v1.1

Quando a v1.1 encontra os dados antigos na mesma origem, ela guarda **uma cópia local** em `arvak-library-backup-before-v1.1`. Essa cópia pode ser baixada em **Dados e backup → Cópia automática da versão anterior**. Ela só existe se o armazenamento local estiver disponível e a versão antiga ainda estiver lá; é uma segurança extra, **não substitui o arquivo JSON salvo no computador**.

## Como marcar projetos

- **Em testes**: clique no projeto → **Situação do projeto** → **Em testes** → **Salvar**.
- **Com bug**: clique no projeto → marque **Com bug** → anote opcionalmente o problema → **Salvar**.
- Você pode marcar **Em testes** e **Com bug** ao mesmo tempo.
- Para filtrar, use os novos botões no menu lateral ou na faixa de filtros.
- Ao adicionar um projeto novo, ambos também estão disponíveis.

## Segurança dos dados

- Atualizar os arquivos do GitHub não apaga automaticamente o `localStorage` do mesmo navegador e domínio.
- Limpar os dados de navegação, usar janela anônima, trocar de domínio ou trocar de aparelho **pode fazer seus dados desaparecerem daquele acesso**.
- A biblioteca não possui conta nem sincronização. Para mover dados entre dispositivos, exporte e importe o JSON.
- Não publique seus backups, pois eles podem conter notas privadas.

## Commit e release

**Commit:** `feat: add testing status, bug flags and safer backups`  
**Tag:** `v1.1.0`  
**Release:** `Arvak Library v1.1.0 — Testing & Bug Tracking`
