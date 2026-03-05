# Project Scaffolding Skill

An [agent skill](https://github.com/vercel-labs/skills) that scaffolds new full-stack projects with customizable CI/CD, dev containers, backend, frontend, and end-to-end testing — all through an interactive conversation.

## What It Does

This skill guides an AI coding agent through an interactive requirements-gathering process and then generates a complete project structure. It supports any combination of:

| Part | Options |
|------|---------|
| **GitHub Actions** | PR build (pre-release), commit build (latest), tag build (stable) |
| **Dev Containers** | Separate per part, unified, or both |
| **Backend** | C# (ASP.NET Core) or Node.js (Express/Fastify), with optional Docker, database, and tests |
| **Frontend** | React+Vite, Next.js, or other; Tailwind/SASS; dark theme; i18n; PWA; fake backend; tests |
| **E2E Testing** | Full-stack Playwright or Cypress tests outside backend/frontend folders |

## Install

```bash
npx skills add <owner>/project-scaffolding-skill
```

Or install to specific agents:

```bash
npx skills add <owner>/project-scaffolding-skill -a claude-code -a cursor -a github-copilot
```

## Usage

Once installed, trigger the skill by asking your AI agent:

- "Create a new project"
- "Scaffold a full-stack app"
- "Bootstrap a project with React frontend and C# backend"
- "Set up a monorepo with CI/CD"

The agent will:

1. Ask which project parts you need (GitHub Actions, Dev Container, Backend, Frontend, E2E)
2. Drill down into each selected part for detailed preferences
3. Show a summary table for confirmation
4. Generate the full project structure with working boilerplate

## Skill Structure

```
skills/
└── project-scaffolding/
    └── SKILL.md
```

## Supported Choices

### Backend

| Choice | Default | Alternatives |
|--------|---------|--------------|
| Language | C# | Node.js |
| Framework (C#) | ASP.NET Core Minimal API | Controller-based API |
| Framework (Node.js) | Express.js | Fastify |
| Database | — | JSON/Text file, SQLite, PostgreSQL, MongoDB, SQL Server |
| Unit test framework (C#) | xUnit | NUnit |
| Unit test framework (Node.js) | Jest | Vitest |

### Frontend

| Choice | Default | Alternatives |
|--------|---------|--------------|
| Build tool | React + Vite | Next.js, other |
| Styling | Tailwind CSS | SASS |
| Component test framework | Jest | Vitest, other |
| Integration test framework | Playwright | Cypress, other |

### E2E

| Choice | Default | Alternatives |
|--------|---------|--------------|
| Framework | Playwright | Cypress, other |

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

MIT
# project-scaffolding-skill
