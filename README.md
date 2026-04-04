# Introduction

This project contains a base Claude Structure for projects.

Using Claude AI to code, it's necessary to create some files to help Claude understand the project, with this, Claude gets better context to make better responses.

For this, there is a default structure to create project documentations and files for Claude read and understand the project.

Since these files are used in all projects, the idea is to create centralized Claude Structure, and use the same structure in all projects.

## Claude Structure

The Claude Structure in the project is:

```
- .claude
    - agents
    - rules
    - skills
    - CLAUDE.md
```

- **.claude/agents**: Used to put specialists agents, used in the prompts to do specific jobs.
- **.claude/rules**: Rules of code, testing, security, business and others.
- **.claude/skills**: Used to automate repetitive process like commits, verifications in the code and others.
- **.claude/CLAUDE.md**: Used create main doc of the project, relate sub files in that main file.

## General rules

- Keep files smaller, with 200 max lines
- Use bullet points to describe items
- Avoid create big paragraphs or texts
- Keep informations concise
