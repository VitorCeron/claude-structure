---
name: commit-helper
description: A skill that helps generate commit messages based on the changes made in a codebase. It analyzes the changes and provides a concise and informative commit message that accurately describes the modifications.
metadata:
  version: "1.0.0"
---

# Generating Commit Messages with commit-helper

## Instructions

1. Run git diff to get the changes made in your codebase.
2. Suggest a clear, conventional commit message:
   - Use the format: `<emoji> <type>: <description>`
   - Types include: feat, fix, docs, style, refactor, test, chore
   - Description should be concise and informative
   - Use table below for reference on types and emojis

## Examples of Conventional Commits

| Tipo             | Emoji | Exemplo de Commit                                                          |
| ---------------- | ----- | -------------------------------------------------------------------------- |
| **feat**         | ✨    | `:sparkles: feat(auth): Implementar sistema de login Task-123`             |
| **fix**          | 🐛    | `:bug: fix(api): Corrigir erro de timeout na requisição Task-456`          |
| **docs**         | 📚    | `:books: docs: Atualizar README com instruções de deploy Task-789`         |
| **style**        | 🎨    | `:art: style(components): Aplicar design system nos botões Task-101`       |
| **refactor**     | ♻️    | `:recycle: refactor(utils): Simplificar função de validação Task-202`      |
| **test**         | 🧪    | `:test_tube: test(auth): Adicionar testes para login Task-303`             |
| **chore**        | 🔧    | `:wrench: chore: Atualizar dependências do projeto Task-404`               |
| **perf**         | ⚡    | `:zap: perf(database): Otimizar consultas de usuários Task-505`            |
| **ci**           | 🧱    | `:bricks: ci: Configurar deploy automático para staging Task-606`          |
| **hotfix**       | 💥    | `:boom: hotfix: Corrigir falha crítica no pagamento Task-707`              |
| **build**        | 📦    | `:package: build: Configurar webpack para produção Task-808`               |
| **revert**       | ⏪    | `:rewind: revert: Reverter mudanças no componente Header Task-909`         |
| **tag**          | 🔖    | `:bookmark: tag: Criar tag de versão v1.2.0 Task-910`                      |
| **construction** | 🚧    | `:construction: construction: Trabalho em progresso no dashboard Task-911` |
| **Merge**        | 🔀    | `:twisted_rightwards_arrows: Merge: mensagem padrão de merge`              |
