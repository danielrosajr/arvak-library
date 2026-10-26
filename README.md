# Arvak Library v1.4.0 — Project Ranking

Biblioteca pessoal de aplicativos, ideias, mods e automações. Agora inclui **Ranking de Projetos**, sem substituir as funções já existentes.

**Site:** https://danielrosajr.github.io/arvak-library/
**Repositório:** https://github.com/danielrosajr/arvak-library

## O que há nesta versão

- Biblioteca de projetos com favoritos, status, busca, links de GitHub, aplicativos e conversas do ChatGPT.
- Projetos manuais, importação e sugestão de repositórios públicos do GitHub.
- Correções, ideias futuras, marcação de bugs, backup e tutorial.
- **NOVO:** 10 critérios de avaliação e manutenção opcional, em notas de 0 a 10, sem pré-preenchimentos inventados.
- **NOVO:** Ranking calculado de 0 a 100 (não é probabilidade de sucesso), com cobertura de pesos e resultados provisórios.
- **NOVO:** 7 perspectivas: geral, comercial, social, pessoal, execução rápida, portfólio e oportunidades.
- **NOVO:** Pesos editáveis no modo geral e em presets personalizados, salvos no navegador.
- **NOVO:** Ranking manual independente com controles de subir/descer, inclusive no celular.
- **NOVO:** Sugestões contextuais simples, com dados que explicam a indicação.
- **NOVO:** Filtro por texto, categoria, status e avaliação insuficiente.
- **NOVO:** Migração sem reformatar o arquivo original; cópia preventiva local antes da v1.4.

## Como acessar

No menu esquerdo, escolha **Ranking de Projetos**. Para avaliar um projeto, clique em **Avaliar**, abra **Avaliação & Prioridade** e selecione apenas as notas que souber responder. É possível adicionar uma justificativa para cada nota. Alterações são salvas imediatamente. Projetos não avaliados mostram “— Não avaliado —”.

## Como a nota é calculada

Defina `s_i` de 0 a 10 e `w_i` como peso não negativo. Dificuldade, esforço e custo de manutenção usam nota ajustada `a_i = 10 − s_i`; os demais usam `a_i = s_i`. No modo **Oportunidades**, a validação real também é invertida: uma validação baixa sinaliza necessidade de investigar a hipótese, não prova de oportunidade comercial.

Para os critérios preenchidos que têm peso maior que zero:

```
indice = round(100 × Σ(w_i × a_i) / (10 × Σ w_i preenchidos))
cobertura = round(100 × Σ(w_i preenchidos) / Σ(w_i de todos os critérios))
```

- **≥ 90%** de cobertura: classificação com boa cobertura.
- **60% até menos de 90%:** classificação provisória.
- **Menos de 60%** (ou pesos totais iguais a zero): aguarda avaliação, sem índice.
- Pesos **não precisam somar 100**; o cálculo normaliza automaticamente. Pesos iguais a zero excluem critérios.
- Empates usam a ordem alfabética como desempate. Pontuações parciais não são misturadas entre projetos com graus de cobertura muito diferentes.

A nota é **um índice subjetivo de prioridade**, não estimativa de receita, probabilidade de sucesso, qualidade ou impacto medido. O usuário tem a decisão final.

## Onde meus dados ficam?

Toda a personalização continua em `localStorage`, na chave existente **`arvak-library-v1`** (`version: 1`). Avaliações e justificativas são guardadas em `state.overrides[projectId].evaluation`. Os pesos e a lista manual ficam em `state.ranking`. Nenhum projeto antigo recebe avaliação automática. A primeira abertura da v1.4 cria, quando possível, uma cópia local do JSON anterior em `arvak-library-backup-before-v1.4`.

O navegador **não sincroniza com outros computadores**. Exporte o backup JSON regularmente em **Dados e backup → Exportar biblioteca**. O backup exporta os campos anteriores e os novos.

## Atualizar sem terminal

Leia [COMO_ATUALIZAR.md](COMO_ATUALIZAR.md). Apenas o `index.html` precisa ser substituído. Para publicar, mantenha GitHub Pages em **Deploy from a branch**, branch `main`, pasta `/ (root)`.

## Stack

HTML, CSS e JavaScript puros, em um único arquivo estático; sem npm, login, banco de dados ou servidor próprio. API pública do GitHub usada apenas para a descoberta/atividade opcional dos repositórios. Não usa IA para pontuar.

## Roadmap

Veja [ROADMAP.md](ROADMAP.md). A próxima versão está planejada para **Project Insights**, sem promessa de integração automática com dados privados.
