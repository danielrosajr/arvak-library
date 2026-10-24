# Arvak Library v1.3.0 — GitHub Discovery

Biblioteca pessoal de apps, mods, ferramentas e ideias, inspirada em uma estante de jogos. **Funciona em um único `index.html`, sem npm e sem backend.**

## Novidade: descobrir projetos do GitHub

- Botões **Buscar projetos** e **Descobrir no GitHub** abrem o scanner.
- Ao abrir a biblioteca, ele consulta automaticamente os repositórios públicos de `danielrosajr` **no máximo uma vez a cada 24 horas** (pode desativar em Dados e backup).
- Ao identificar repositórios que não constam no catálogo inicial nem nos seus cadastros pessoais, mostra sugestões com nome, descrição, linguagem, último push, fork/arquivado e indicação de GitHub Pages habilitado.
- Você pode **Adicionar à biblioteca** ou **Ignorar sugestão**. As ignoradas podem ser exibidas novamente pela caixa **Mostrar ignorados**.
- Nenhum projeto é adicionado sem sua escolha. O status inicial dos importados é **A organizar**, pois o GitHub não informa o estágio real do desenvolvimento.
- O scanner associa um repositório já cadastrado pelo nome de repositório ou por sua URL GitHub. Se um cadastro manual não tiver endereço GitHub, pode ser sugerido de novo; associe a URL para evitar isso.
- Quando um repositório tem GitHub Pages habilitado, há uma opção para incluir o endereço padrão. **Pages habilitado não garante que o endereço realmente funcione.** Confira antes de marcar.
- A busca também atualiza a data do último push dos projetos conhecidos, sem tocar em seus status, favoritos ou anotações.

## Privacidade e limites

Utiliza a API pública do GitHub (`GET /users/danielrosajr/repos`). Não requer token, login, servidor ou chaves secretas. Detecta apenas **repositórios públicos**; privados não são descobertos.

O GitHub limita a quantidade de solicitações sem autenticação (normalmente 60/hora por IP, sujeito a alterações). Ao atingir o limite ou ficar offline, a biblioteca continua funcionando e o scanner mostra um aviso. Suporta até 500 repositórios consultados na mesma busca, em até cinco páginas de 100.

Os dados da biblioteca ficam no `localStorage` do navegador. A coleção não é enviada ao GitHub. O scanner salva apenas metadados públicos e suas preferências de sugestões. Não coloque tokens de acesso no HTML.

## Manutenção e publicação

Basta enviar `index.html` à raiz do repositório `danielrosajr/arvak-library` e manter GitHub Pages configurado como **Deploy from a branch → main → /(root)**. Consulte `COMO_ATUALIZAR.md` antes de atualizar.

## Recursos mantidos

- Biblioteca com busca, filtros, favoritos, status **Em andamento / Em testes / Pausado / Concluído / Ideia / Arquivado**
- Marcação independente **Com bug** e anotações
- Correções pendentes e ideias futuras
- Links rápidos para o app, repositório e conversa do ChatGPT
- Tutorial guiado, temas, modo cartão/lista
- Backup e restauração JSON, inclusive arquivos das versões anteriores

**Licença:** não definida nesta versão.
