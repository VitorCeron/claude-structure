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
| **feat**         | ✨    | `:sparkles: feat(auth): new feature implemented`                  |
| **fix**          | 🐛    | `:bug: fix(api): fix error on request`                            |
| **docs**         | 📚    | `:books: docs: update README`                                     |
| **style**        | 🎨    | `:art: style(components): apply design system on buttons`         |
| **refactor**     | ♻️    | `:recycle: refactor(utils): refactor utility functions`           |
| **test**         | 🧪    | `:test_tube: test(auth): login tests added`                       |
| **chore**        | 🔧    | `:wrench: chore: update project dependencies`                     |
| **perf**         | ⚡    | `:zap: perf(database): otimize queries`                           |
| **ci**           | 🧱    | `:bricks: ci: deploy settings staging`                            |
| **hotfix**       | 💥    | `:boom: hotfix: fix critical issue on payment`                    |
| **build**        | 📦    | `:package: build: production webpack settings`                    |
| **revert**       | ⏪    | `:rewind: revert: revert changes`                                 |
| **tag**          | 🔖    | `:bookmark: tag: create tag to version v1.2.0`                    |
| **construction** | 🚧    | `:construction: construction: Work in progress`                   |
| **Merge**        | 🔀    | `:twisted_rightwards_arrows: Merge: merge message`                |
| **tada**         | 🎉    | `:tada: tada: first commit`                                       |
| **wheelchair**   | ♿    | `:wheelchair: accessibility`                                      |
| **lock**         | 🔒️    | `:lock: lock: security changes`                                   |

