# Atualizar a Arvak Library para a v1.6.0 pelo GitHub (sem terminal)

A v1.6 utiliza **um único arquivo HTML** para rodar. Não crie outro repositório nem altere a configuração do GitHub Pages.

1. Abra sua biblioteca publicada: <https://danielrosajr.github.io/arvak-library/> **no mesmo navegador em que estão seus projetos e anotações**.
2. Entre em **Dados e backup → Exportar biblioteca** e guarde o arquivo `.json` em uma pasta segura. É essencial, pois suas alterações pessoais existem no navegador, não no HTML publicado.
3. Baixe o `index.html` desta nova versão.
4. Acesse <https://github.com/danielrosajr/arvak-library/blob/main/index.html>.
5. Clique no lápis (**Edit this file**), selecione todo o conteúdo antigo e substitua pelo conteúdo do novo `index.html`. Alternativamente, use `github.dev` para substituir o arquivo. Mantenha o nome e o caminho exatamente como estavam.
6. Clique em **Commit changes** na branch `main`. Mensagem sugerida:
   `feat: add Idea Vault with reusable prompts and project vision notes`
7. Acesse a biblioteca e faça uma recarga de página. Verifique **Cofre de Ideias** no menu lateral.
8. Teste em um projeto antigo e verifique favoritos, bugs, links, rankings e outros dados. Em seguida, crie uma nova ideia de teste, salve um prompt e confira se ele persiste ao recarregar a página.

### Se algo estiver faltando

Use **Dados e backup → Importar biblioteca** e selecione o backup JSON que você exportou antes da atualização. A aplicação mostrará uma prévia e pedirá confirmação. **A importação substitui os dados pessoais atuais**. Não faça isso se você já criou novos projetos e não os exportou antes.

### O que deve ser substituído?

| Arquivo | Ação |
|---|---|
| `index.html` | **Substituir** |
| `README.md` | Atualização opcional da documentação |
| `CHANGELOG.md`, `ROADMAP.md`, `RELEASE_NOTES.md` | Adicionar apenas se quiser manter a documentação no GitHub |
| Configuração do GitHub Pages | **Não alterar** |

### Segurança dos prompts

- O Cofre não envia suas ideias automaticamente para serviços externos.
- O backup `.json` inclui prompts e notas e deve ser armazenado em um local privado.
- O comando **Copiar prompt** coloca texto na sua área de transferência; você escolhe se quer colá-lo no ChatGPT.
- Uma ideia que passa para `Em andamento` continua aparecendo no Cofre enquanto existir conteúdo salvo.
