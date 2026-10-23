# ARVAK LIBRARY — Minha biblioteca pessoal

Uma estante particular dos projetos do Daniel, inspirada na biblioteca de jogos de uma loja digital. **Este é um aplicativo separado do Arvak Labs público.**

## O que existe nesta versão (v1.0)

- 11 projetos iniciais provenientes dos repositórios públicos consultados em 23/10/2026 (inclui o Arvak Labs).
- Acesso rápido aos 3 projetos usados recentemente (ou aos mais atualizados, enquanto não houver histórico).
- Cartões coloridos com atalhos para o site e/ou GitHub.
- Marcar favoritos e organizar por situação: **A organizar, Ativo, Pausado, Concluído, Ideia, Arquivado**.
- Próximo passo e anotações por projeto.
- Pesquisa, categorias, ordenação e visualização em cartões ou lista.
- Filtro **Sem atualização** para projetos sem push público no GitHub há 30 dias ou mais. **Um período sem push não significa que o projeto está pausado ou abandonado.**
- Botão **Atualizar atividade**: consulta a API pública do GitHub para atualizar somente as datas do último push. Não altera seus status nem suas notas. Pode falhar sem internet ou por limite de requisições.
- Adicionar projetos próprios, inclusive ideias sem repositório.
- Tema claro/escuro e layout mobile.
- Backup exportável/importável em JSON.
- Sem frameworks, npm, banco de dados, cadastro ou servidor.

## Para abrir agora (sem instalar nada)

1. Baixe e extraia o ZIP.
2. Abra **`index.html`** com um navegador moderno (Chrome, Firefox etc.).
3. Clique em **Abrir app** para abrir o site publicado, ou **Ver código** nos projetos sem site registrado.
4. Use os três pontinhos de um cartão para alterar situação, anotar próximos passos e mudar os links.

> Algumas restrições de navegador no modo `file://` podem afetar o armazenamento local. Se possível, publique no GitHub Pages para ter armazenamento mais previsível.

## Publicar no GitHub Pages pelo navegador, sem comandos

Recomendado: **criar outro repositório** chamado `arvak-library`. Assim você **não substitui** o Arvak Labs já publicado em `danielrosajr.github.io`.

1. Entre em https://github.com/new . Nome: `arvak-library`. Selecione **Public**. Marque **Add a README file** (opcional, facilita acesso ao menu de upload). Clique em **Create repository**.
2. Abra a raiz do repositório, **Add file → Upload files**, e carregue **`index.html` extraído** (não envie o ZIP como arquivo único). Faça commit na branch `main`.
3. Abra **Settings → Pages → Build and deployment**.
4. Em **Source**, selecione **Deploy from a branch**, em **Branch** selecione **`main` / `(root)`** e clique em **Save**.
5. Quando a publicação terminar, o endereço esperado é `https://danielrosajr.github.io/arvak-library/`.
6. Como esse aplicativo tem apenas um `index.html` com CSS e JS embutidos, ele **não precisa** do workflow do Vite ou do GitHub Actions que usamos no Arvak Labs.

### Atualizações futuras

Abra `index.html` no repositório → clique no lápis (Edit file) → cole o novo conteúdo → **Commit changes**. Ou faça upload de nova versão com o mesmo nome no diretório raiz. Quando editar o conteúdo, não altere sua URL publicada.

### Quer acesso só para você?

O repositório e a interface no Pages são públicos quando hospedados dessa forma. **As suas notas e escolhas pessoais não são enviadas ao repositório nem ficam públicas**; permanecem no armazenamento deste navegador. Não coloque dados privados nos arquivos HTML do repositório.

## Onde ficam seus dados pessoais?

Em `localStorage` no navegador, com a chave `arvak-library-v1`. Isso significa:

- Marcar um projeto como **Pausado** no computador **não vai** mudar o status no seu celular automaticamente.
- Se o navegador apagar seus dados do site, você pode perder suas anotações.
- Use **Dados e backup → Exportar** para salvar um JSON periodicamente; para transferir a outro navegador ou dispositivo use **Importar**.
- A **importação substitui** as personalizações existentes no navegador de destino.
- Se você publicar outra cópia em um endereço diferente, ela terá armazenamento local separado.

## Como atualizar a lista de repositórios inicial

A lista base é a constante `defaults` perto do início da tag `<script>` em `index.html`. Não é preciso editar isso para acrescentar um projeto pessoal: use o botão **+ Novo projeto** no próprio aplicativo (o projeto ficará somente no navegador e nos backups).

Os links de aplicativos foram preparados apenas para os projetos que, durante a consulta em 23/10/2026, tinham GitHub Pages habilitado. **Isso não garante que o deploy de todos eles esteja funcionando**. Nos projetos sem Pages registrado, o botão leva ao repositório. Edite o link no painel do projeto se ele tiver um site diferente.

## Privacidade e limitações

O aplicativo não executa login e não manda notas, tags, situações ou histórico de abertura para nenhum servidor. Clicar em links abre serviços externos (GitHub ou páginas individuais). O botão de atualização de atividade consulta `api.github.com` com os nomes dos repositórios públicos. Nenhum token ou segredo de acesso é usado.

**Licença:** não definida.
