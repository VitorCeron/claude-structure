# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

This project is an CRUD of users to enable the admin to manage users data.

## Stack

- Node.js 20+
- Postgres
- Jest

## Commands

```bash
# Development
npm run dev              # Run the project local
npm run build            # Compile TypeScript to dist/
npm start                # Run compiled server

npm test                 # Run all tests
```

## Architecture

[Architecture of project, folders structure, main principles of architecture]

```
- src
    - [module]
        - __tests__
        - module.controller.ts
        - module.service.ts
        - module.repository.ts
        - module.router.ts
        - module.types.ts
    - docs
    - middleware
    - routes
    - utils
    - app.ts
    - server.ts
```

- **module:** Used to create complete module for example: `users`, `authentication`, `health`.
- **module.controller.ts:** Used to handle requests and direct to correct service or method.
- **module.service.ts:** Used to keep business logic layer.
- **module.repository.ts:** Used to database layer, only here it's possible call database.
- **module.types.ts:** Used to put specific types from this module.
- **module.router.ts:** Used to keep module routes.
- **docs:** Used to docs from all application.
- **middleware:** Used to handle requests before comes to controller, authorization and etc.
- **routes:** General routes from app.
- **utils:** Utils functions can be used whole application.
- **app.ts:** General app file.
- **server.ts:** General server file.

## Agents

- [Node.js Specialist](.claude\agents\nodejs-specialist.md)

## Skills

- [Commit Helper](.claude\skills\commit-helper\skill.md)
- [Npm Upgrader](.claude\skills\npm-upgrader\skill.md)

## Rules

- [Code Styles](.claude\rules\nodejs-code-styles.md)
- [Testing](.claude\rules\nodejs-testing.md)
