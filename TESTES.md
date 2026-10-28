# Validação da Arvak Library v1.7.0

Testes locais executados com Chromium headless carregando o HTML e simulando armazenamento `localStorage` e respostas do GitHub. **Não** equivalem a um teste no site publicado.

## Verificado

- Sintaxe do JavaScript (Node.js v22) sem erros.
- Renderização desktop e mobile (390 px); sem rolagem horizontal na área principal verificada.
- Matriz com três avaliações sintéticas completas e filtro por categoria; itens sem cobertura suficiente não aparecem como pontuados.
- Comparação e simulador de cenários; simular outro preset não altera `state.ranking.mode`.
- Sessão do Duelo: iniciar, selecionar preferência, desfazer, pausar, fechar, reabrir, concluir e aplicar.
- Projetos pausados/concluídos aparecem ao final da prioridade manual; ação Reativar disponível.
- Persistência de uma rodada após abrir a biblioteca novamente com o JSON exportado do estado salvo.
- Compatibilidade com um conjunto sintético v1.6 contendo projeto adicionado manualmente, favorito, notas, prompt do Idea Vault, texto privado e ranking anterior.
- Snapshot local pré-v1.7 criado na primeira abertura quando existia backup prévio.
- Pesos em zero retornam índices não calculados, não NaN.
- Valores de projeto com HTML especial são escapados ao renderizar o ranking.

## Ainda precisa de validação no site publicado

- Abra o GitHub Pages com seu armazenamento real, confira a coleção, os links e o backup.
- Verifique o Duelo em um celular físico, especialmente a rolagem da janela.
- Teste manualmente importar um backup JSON real salvo pela sua v1.6.
- Teste o scanner do GitHub, que depende da API pública e de rede externa.
