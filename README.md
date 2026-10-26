# Arvak Library v1.5.0 — Smart Rank

Biblioteca pessoal de apps, jogos, mods, ferramentas e ideias, com avaliações e rankings de projetos. **Agora com análise assistida pelo ChatGPT gratuito, sem chave de API.**

## Novidades da v1.5

- **Smart Rank**, acessível pelo menu lateral ou em **Ranking de Projetos**.
- Gera um prompt estruturado para avaliar projetos com o ChatGPT. Você cola o prompt no ChatGPT e importa o JSON devolvido.
- Três escopos: todos, pouco avaliados (cobertura abaixo de 90%) ou novos/alterados após a última importação aprovada.
- Cinco contextos de análise: equilibrado, comercial, social, portfólio e execução rápida.
- Pode consultar os READMEs públicos via API do GitHub. Se indisponíveis, continua com metadados; **não afirma ter inspecionado o código**.
- Prévia do prompt antes de compartilhá-lo; botão de copiar e download TXT.
- Importação de JSON colado ou arquivo, com validação de formato, nome/ID do projeto, notas numéricas de 0 a 10 e projetos desconhecidos.
- Prévia comparativa nota anterior → sugestão, justificativa, confiança e evidência.
- Notas previamente avaliadas começam **desmarcadas**; critérios pessoais (importância, motivação e urgência) também são desmarcados por padrão.
- Aplicação por seleção e confirmação explícita, sem apagar campos não selecionados.
- Guarda origem, data, confiança e referência textual das avaliações aceitas; edição manual remove a indicação de origem IA para o critério modificado.
- Registro de novas/alteradas baseado em dados locais do projeto, inclusive último push recuperado do GitHub.
- Cópia preventiva local do estado anterior à v1.5 e compatibilidade com backup da v1.4.

## Fluxo em 5 passos

1. Entre na [Arvak Library](https://danielrosajr.github.io/arvak-library/) e exporte um backup em **Dados e backup**.
2. Acesse **Smart Rank → Gerar prompt**. Decida se deseja incluir READMEs públicos.
3. Confira a prévia, copie e cole o prompt em [ChatGPT](https://chatgpt.com/). Peça ao ChatGPT para devolver apenas o JSON especificado.
4. Copie o JSON da resposta na Arvak Library → **Validar e comparar**.
5. Selecione as notas que concorda em aceitar e clique em **Aplicar selecionadas**. A pontuação do ranking v1.4 é recalculada normalmente, usando seus pesos atuais.

**Importante:** ChatGPT é utilizado pelo usuário em outra aba. A biblioteca **não invoca uma API de IA e não gera avaliações sozinha**. O ChatGPT gratuito pode ter limites de tamanho e de uso. Projetos e notas não são enviados automaticamente; o compartilhamento ocorre ao copiar o prompt no ChatGPT.

## Limites de segurança e qualidade

- Apenas dados do projeto necessários ao prompt: nome, descrição, categoria, status, tecnologias e URL pública do repositório. Não são incluídos os campos privados de notas, favoritos, tarefas, bugs nem URLs das conversas ChatGPT. Os READMEs são arquivos **públicos** e podem conter texto adicional: sempre revise a prévia antes de compartilhar.
- Os READMEs são limitados a 10.000 caracteres por projeto; não há clone do repositório, auditoria do código ou inferência automática de usuários e receitas.
- Critérios não verificados ficam **não avaliados**. A avaliação não é uma previsão objetiva de sucesso.
- Maturidade técnica e dificuldade podem ser estimadas, mas esforço restante, monetização e impacto social são hipóteses e exigem cautela.
- GitHub público possui limites por IP e pode negar requisições; nesses casos o prompt continua utilizável com metadados.
- O JSON colado permanece na tela até você fechá-la. As sugestões só são gravadas após seleção e confirmação explícita.

## Tecnologia

HTML/CSS/JavaScript, tudo em um único `index.html`. Sem npm, banco de dados, chaves de API ou backend. Compatível com GitHub Pages **Deploy from a branch**.

### Dados e backups

Chave histórica **`arvak-library-v1`**, `version: 1`. Novas informações ficam em `smartRank` e em `overrides[id].evaluation`, mantendo o formato anterior. Há cópia local opcional em `arvak-library-backup-before-v1.5`.

Faça backup JSON antes de qualquer atualização. A biblioteca usa o armazenamento do navegador e não sincroniza entre dispositivos.

### Fórmula do ranking (mantida da v1.4)

Índice = soma dos `(nota convertida / 10) × peso` dos critérios preenchidos, dividida pela soma dos pesos preenchidos, multiplicada por 100. Em `difficulty`, `effort` e `maintenance`, a nota convertida é `10 - nota`. Cobertura = soma dos pesos respondidos / soma de todos os pesos ativos. Projetos abaixo de 60% de cobertura não recebem índice; entre 60% e 90% recebem rótulo provisório. Pesos zerados não geram divisão por zero.

## Instalação e publicação

Consulte [`COMO_ATUALIZAR.md`](COMO_ATUALIZAR.md). No repositório `danielrosajr/arvak-library`, atualize apenas o `index.html` na raiz e faça commit na branch `main`. Não precisa mudar o modo de GitHub Pages.

## Roadmap

Veja [`ROADMAP.md`](ROADMAP.md). Esta versão é a **v1.5.0 — Smart Rank**. A próxima proposta é **v1.6.0 — Project Insights**.

## Licença

Nenhuma licença foi definida nesta entrega; o repositório não recebe uma licença automaticamente.
