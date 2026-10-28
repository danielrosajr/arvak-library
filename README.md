# Arvak Library v1.7.0 — Project Insights & Priority Duel

Biblioteca pessoal de aplicativos e ideias, feita em **um único `index.html`** (HTML, CSS, JavaScript). Não exige npm, build, login, backend nem API paga.

**Nova nesta versão:**

- **Project Insights:** dashboard com números por fase, recomendações de regras explicáveis, matriz Impacto × Esforço, comparação de 2–3 projetos e simulação de cenários sem alterar os pesos salvos.
- **Duelo de Prioridades 1×1:** confronto entre dois projetos por rodada para ordenar o ranking manual de forma eficiente (inserção binária, tipicamente O(n log n), considerando preferências consistentes). A classificação calculada continua independente.
- **Pausar / Concluir durante o duelo** e diretamente no ranking manual. Pausados/concluídos aparecem no fim do ranking. **Reativar** também está disponível.
- **Desfazer rodada**, continuar sessão depois, conferir resultados e aplicar a nova ordem somente ao confirmar. Fechar o duelo não encerra a sessão.
- **Backup pré-v1.7 automático local**, sem remover versões antigas ou mudar a chave original de armazenamento.

## Importante: preservação de dados

A aplicação continua usando a chave **`arvak-library-v1`** e o esquema `version: 1` para manter compatibilidade com backups antigos. O novo duelo é salvo em `ranking.duel` e o ranking manual em `ranking.manual`; os demais campos continuam iguais.

Dados locais não sincronizam automaticamente entre dispositivos. **Exporte um JSON na versão antiga antes de atualizar.** A v1.7 oferece cópia local pré-atualização, mas essa cópia pode ser perdida se o navegador for limpo.

Se marcar Pausado/Concluído no duelo, o **status é salvo imediatamente**. Descartar a ordenação não reverte mudanças de status (elas podem ser revertidas com Reativar). A ordenação inteira somente é substituída após clicar em **Aplicar minha nova ordem**.

## Como usar o Duelo

1. Abra **Ranking de Projetos → Priorizar em duelos 1×1**.
2. Escolha qual projeto prefere priorizar a cada par. Não é uma competição por maior número de vitórias: uma inserção binária coloca os itens progressivamente na ordem.
3. Use **Manter ordem anterior neste duelo** para aceitar a ordem atual daquele par sem deliberar novamente.
4. Use **Pausar** ou **Concluir** em qualquer um dos dois projetos para tirá-lo das próximas comparações e deixá-lo ao fim.
5. Pode fechar o painel e continuar depois. **Desfazer rodada** recupera até 100 estados anteriores da sessão.
6. Confira a ordem final e clique em **Aplicar minha nova ordem**. Se optar por descartar, a ordem anterior permanece, exceto mudanças explícitas de status.

## Como usar Insights

- **Matriz:** escolha perspectiva (geral/comercial/social/pessoal/portfólio), categoria e situação; o eixo X é esforço (dificuldade + esforço até MVP) e o Y é impacto ponderado, com linhas em 5/10. Exige notas de dificuldade **e** esforço e cobertura de impacto >=60%; demais itens são mostrados como sem dados suficientes. Quadrantes são heurísticas de planejamento.
- **Comparação:** escolha 2–3 projetos; veja notas reais e campos não avaliados, sem substituição por zero.
- **Cenários:** escolha pesos gerais, comerciais, sociais, pessoais, portfólio, execução rápida ou oportunidades. Uma simulação não muda a configuração global ou a prioridade manual. Projetos com baixa cobertura não são pontuados.
- **Sugestões:** exclusivamente regras explicáveis baseadas em status e avaliações preenchidas. Não representam previsão de sucesso.

## GitHub Pages

O endereço esperado é `https://danielrosajr.github.io/arvak-library/` caso as configurações do Pages permaneçam habilitadas. Consulte `COMO_ATUALIZAR.md` antes de alterar o site.

### Estrutura

```
index.html              # Aplicação completa (atualizar só ele)
README.md               # Este guia
COMO_ATUALIZAR.md       # Passo a passo no navegador
RELEASE_NOTES.md        # Conteúdo para GitHub Release
CHANGELOG.md            # Histórico
ROADMAP.md              # Próximos passos
TESTES.md               # Validações e testes manuais
PREVIA-*.png            # Imagens demonstrativas opcionais
```

## Privacidade e limites

Todos os dados pessoais são armazenados no navegador. A área Insights e o Duelo não usam rede. Funcionalidades anteriores como o scanner opcional do GitHub e leitura de README pelo Smart Rank ainda podem consultar endpoints públicos; nada disso é necessário para usar os Insights.

O aplicativo não verifica se notas subjetivas são corretas; o ranking mede as avaliações registradas, não sucesso futuro. Projetos não avaliados ficam indicados como tal.
