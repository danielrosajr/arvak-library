# Atualizar Arvak Library para a v1.5.0, sem terminal

## 1. Proteger seus dados atuais

Abra a **Arvak Library antiga** no mesmo navegador em que você cadastrou seus projetos:

https://danielrosajr.github.io/arvak-library/

Clique em **Dados e backup → Exportar biblioteca**. Guarde o `.json` fora da pasta de downloads temporários. Isso é crucial para projetos criados por você, notas, links de conversas, ranking, correções e ideias.

## 2. Substituir o aplicativo

1. Abra: https://github.com/danielrosajr/arvak-library
2. Na raiz, abra o arquivo `index.html`.
3. Use o lápis **Edit this file**. Substitua todo o conteúdo pelo `index.html` desta versão (baixe o arquivo separadamente se preferir).
4. Clique em **Commit changes**, mantendo a branch `main`.
5. Se houver limitação de tamanho do editor web, use **Add file → Upload files** para subir o `index.html` extraído do ZIP, confirmando a substituição quando a interface permitir. Nunca faça upload do ZIP fechado como se fosse o site.
6. Abra **Settings → Pages** e confira se ainda está em **Deploy from a branch → main → /(root)**. Se já funciona, não altere essa configuração.
7. Verifique o site publicado. Se a versão antiga persistir, atualize a aba sem cache (Ctrl + Shift + R).

## 3. Primeira execução

- Verifique que todos os projetos manuais, notas, favoritos, conversas do ChatGPT e rankings continuam presentes.
- Em **Ranking de Projetos → Smart Rank**, escolha o escopo.
- De preferência, faça o primeiro teste com **Somente projetos pouco avaliados** e READMEs públicos desmarcados. Depois marque a opção de READMEs para análises mais fundamentadas.
- Clique **Gerar prompt** e abra a prévia para revisar o texto.
- Clique **Copiar prompt**, abra o ChatGPT e cole. O serviço pode responder em vários blocos; junte apenas JSON compatível antes de importar.
- Copie a resposta JSON inteira para **Importar sugestões**, clique **Validar e comparar**, confira as notas propostas e marque apenas as que concordar.
- Clique **Aplicar selecionadas** e confirme.

## 4. Solução de problemas

**Apareceu projeto sem avaliação?** É esperado. Critérios com evidência insuficiente ficam em branco, não em zero.

**O ChatGPT não trouxe um JSON válido?** Responda na mesma conversa: “Devolva apenas um objeto JSON válido, sem explicação e sem markdown, seguindo o schema arvak-smart-rank-v1 e os mesmos ids.”

**Erro em projeto desconhecido?** Confira se cada objeto tem o campo `id` exatamente igual ao usado no prompt; o app não cria projetos por importação de sugestões.

**Leitura do README falhou?** Desmarque a opção README, ou tente novamente depois. A API pública do GitHub tem limites e pode não disponibilizar o arquivo.

**Sumiço dos dados?** Verifique se está no mesmo navegador/endereço. Use **Dados e backup → Importar backup** para restaurar o JSON antigo com confirmação. A v1.5 também tenta guardar cópia local na primeira abertura.

## 5. Metadados para GitHub

- **Repository:** `arvak-library`
- **Commit:** `feat: add free AI-assisted Smart Rank with JSON review`
- **Tag:** `v1.5.0`
- **Release title:** `Arvak Library v1.5.0 — Smart Rank (Free AI Workflow)`
- **Description:** `A personal project library with GitHub discovery, AI-assisted rankings, development tracking, bug lists, and ChatGPT links.`
- **Topics:** `app-library`, `project-ranking`, `ai-assisted`, `github-api`, `github-pages`, `local-first`, `javascript`, `productivity`

Nenhuma publicação ou alteração no seu repositório foi realizada durante esta entrega.
