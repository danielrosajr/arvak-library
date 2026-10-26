# Changelog — Arvak Library

## [1.6.0] — Idea Vault

### Added
- Área **Cofre de Ideias** para projetos ainda não iniciados.
- Campos por projeto para prompt completo (40 mil caracteres), origem/motivação, resultado final desejado e notas/referências.
- Etapas independentes de preparação: **Rascunho**, **Estruturada** e **Pronta para começar**.
- Salvamento automático, botão de salvar manual, contador de caracteres e data de última edição.
- Copiar, exportar TXT e importar TXT com confirmação antes de substituir texto existente.
- Painel de ideias com busca textual, filtros, ordenação e indicadores.
- Fluxo "Guardar nova ideia" que cria o projeto com status **Ideia** e abre o editor.
- Nova etapa no tutorial guiado para explicar o Cofre.
- Cópia preventiva local antes da atualização para a v1.6.

### Changed
- Ideias inteiras agora têm área própria, separada da lista antiga de futuras funcionalidades.
- O Cofre acompanha um projeto mesmo após mudar de **Ideia** para **Em andamento**.
- Backup JSON agora inclui as novas informações; importação de backup reconhece esses campos quando presentes.
- Roadmap adiado: Project Insights visual para v1.7.

### Preserved
- Mesma chave `arvak-library-v1` e formato geral `version: 1`, evitando migração destrutiva.
- Smart Rank, ranking manual e automático, presets, favoritos, links, scanner do GitHub, bugs, correções, tarefas e tutoriais.

### Notes
- Informações são locais, sem sincronização automática entre aparelhos.
- Não há inteligência artificial embutida nem uso de API paga nessa versão; o Cofre armazena o prompt para utilização posterior.
