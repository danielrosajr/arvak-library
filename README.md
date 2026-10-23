# Arvak Library v1.1.0

Sua biblioteca pessoal de aplicativos, mods, ferramentas e experimentos — como uma estante de jogos, mas para os seus projetos.

## Novidades desta versão

- **Em testes**: nova situação de desenvolvimento.
- **Com bug**: marcador independente, com campo para anotar os problemas encontrados. Um projeto pode estar **Em testes e Com bug** ao mesmo tempo.
- Seções e filtros específicos para projetos em teste e com bugs, com contadores no painel.
- Ao adicionar um projeto, você já pode marcá-lo Em testes e/ou Com bug.
- Compatibilidade com dados e backups da v1.0.
- Uma cópia preventiva do estado anterior é guardada no mesmo navegador no primeiro acesso à v1.1, desde que os dados v1.0 estejam disponíveis.
- Lembrete para baixar um backup JSON caso você tenha projetos criados manualmente.
- Importações e redefinições guardam uma cópia de recuperação local antes da substituição (isso **não** substitui um backup JSON baixado).

## Preservando seus projetos

**Antes de atualizar:** entre na sua Arvak Library atual no navegador em que criou os projetos. Abra **Dados e backup → Exportar biblioteca** e guarde o arquivo JSON. Isso é o mais seguro.

Depois, substitua apenas o `index.html` do repositório `arvak-library` pela nova versão e publique no mesmo endereço: `https://danielrosajr.github.io/arvak-library/`.

A v1.1 mantém intencionalmente a chave `localStorage` **`arvak-library-v1`** e a versão de esquema **`1`**. Com o mesmo navegador, mesmo dispositivo e mesmo endereço do GitHub Pages, a atualização do código **não deve** apagar os projetos e notas. Não use **Restaurar biblioteca inicial** e não limpe os dados do site se quiser preservá-los.

A biblioteca não tem sincronização automática: se você trocar de navegador, computador, celular, abrir a versão como `file://` ou alterar o domínio, poderá ver uma coleção diferente. Nesse caso, restaure usando **Dados e backup → Importar backup**. **A importação substitui** as personalizações atuais; exporte-as primeiro.

## Dados e privacidade

- Não há backend, login ou banco de dados.
- As personalizações são guardadas no navegador: projetos adicionados, favoritos, situação, marcação de bug, descrição do bug, notas, links e histórico de acesso.
- O GitHub público **não recebe seus dados pessoais** ao salvar na biblioteca.
- O botão **Atualizar atividade** consulta apenas as datas de push público dos repositórios, quando possível.
- O backup em JSON pode conter anotações pessoais. Guarde-o com cuidado e não o suba para um repositório público.

## Como publicar

É um aplicativo estático em **um único `index.html`**, sem necessidade de Vue, Vite, instalação ou build.

1. Abra `https://github.com/danielrosajr/arvak-library`.
2. Substitua **somente** o arquivo `index.html` na raiz pelo arquivo desta versão e confirme o commit.
3. Confira em **Settings → Pages** que a fonte é **Deploy from a branch**, `main`, `/ (root)`.
4. Abra `https://danielrosajr.github.io/arvak-library/` e recarregue a página.
5. Confira se seus projetos e notas anteriores continuam lá antes de criar novos dados.

Veja `COMO_ATUALIZAR.md` para o guia completo de proteção e recuperação dos dados.

## Tecnologia

HTML, CSS e JavaScript puro; interface responsiva, funcionamento local, sem dependências e publicação gratuita via GitHub Pages.

## Metadata sugerida para o GitHub

**Repository name:** `arvak-library`  
**Description:** `A personal, Steam-inspired library to organize, test, track bugs, and quickly access my apps, mods, and side projects.`  
**Topics:** `app-library`, `project-tracker`, `personal-dashboard`, `bug-tracking`, `local-first`, `javascript`, `github-pages`, `productivity`  
**Version / tag:** `v1.1.0`  
**Commit message:** `feat: add testing status, bug flags and safer backups`  
**Release title:** `Arvak Library v1.1.0 — Testing & Bug Tracking`  
**Website:** `https://danielrosajr.github.io/arvak-library/`

Licença não especificada.
