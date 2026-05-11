# AI Assistant Tools Template (OpenSpec + Agents + Skills)

This repository is a reusable template for AI assistant tooling and spec-driven workflow setup.

It is not an application and it contains no product source code.
It is a baseline to bootstrap assistant behaviors, prompts, skills, and OpenSpec conventions.

## Purpose

This template provides a baseline for:

- AI assistant instruction systems
- OpenSpec-based workflow orchestration
- Agent role definitions
- Prompt and skill standardization
- Reusable project governance for future products

## Quick Start
### 1. Clone and Install

```bash
git clone <repository-url>
cd saas-ai-scaffold
npm install
```

Install OpenSpec globally (required for the spec-driven workflow):

```bash
npm install -g @fission-ai/openspec@latest
```

### 2. Configure Environment

Copy `.env.example` to `.env.local` and fill in your values:

```bash
cp .env.example .env.local
```

See [setup.md](setup.md) for detailed setup steps.

### 3. Start Development

```bash
npm run dev
```

Open http://localhost:5173/ in your browser.

## Create your backlog
  Ask IA for help on populating docs/06-product.md and BACKLOG.md

## Development Workflow

See [BACKLOG.md](BACKLOG.md) for the full feature list and [CONTRIBUTE.md](CONTRIBUTE.md) for the step-by-step workflow guide.


## Target Stack (For Projects Created From This Template)

### Frontend

- React
- Vite
- TypeScript
- TailwindCSS

### Backend (BaaS)

- Supabase
- PostgreSQL
- Supabase Auth
- Row Level Security (RLS)
- Supabase Storage

### Hosting

- Vercel

### Email

- Resend

## Architecture Overview

See [docs/architecture/](docs/architecture/) for the full technical documentation:

- [00-overview.md](docs/architecture/00-overview.md) — System overview and architecture decisions
- [01-frontend.md](docs/architecture/01-frontend.md) — Frontend stack and structure
- [02-backend-supabase.md](docs/architecture/02-backend-supabase.md) — Supabase and data access layer
- [03-auth-security.md](docs/architecture/03-auth-security.md) — Auth flow and security model
- [04-database.md](docs/architecture/04-database.md) — Database schema and conventions
- [05-infra-deployment.md](docs/architecture/05-infra-deployment.md) — Infrastructure and deployment
- [06-product-prd.md](docs/architecture/06-product-prd.md) — Product definition (customize per project)


### OpenSpec files in this repository

This repository uses OpenSpec for spec-driven feature development.

Official docs: https://github.com/Fission-AI/OpenSpec

| Path | Purpose |
|---|---|
| `openspec/config.yaml` | Project configuration and domain rules |
| `openspec/changes/` | Active changes being worked on |
| `openspec/changes/archive/` | Completed and archived changes |
| `openspec/specs/` | Baseline capability specs |
Note: This repository stores the OpenSpec workflow scaffolding itself. No implemented product features exist yet.

## Project Structure

```text
.github/
  agents/          # agent definitions (architect, frontend, backend, qa)
  prompts/         # OpenSpec workflow prompts
  skills/          # reusable skills
  copilot-instructions.md

docs/
  architecture/    # project architecture docs

openspec/
  config.yaml
  changes/
  specs/

README.md
BACKLOG.md
CONTRIBUTE.md
setup.md
```

Note: There is no src/ directory yet because this template is focused on assistant tooling and process setup.

## AI Agents

This repo includes specialized development agents:

- Architect: system design and decisions
- Frontend: UI and client logic
- Backend: Supabase and data layer
- QA: testing and validation


## Notes

This template is intentionally minimal in product definition.
It is designed to be reused across projects by changing AI tooling configuration and OpenSpec artifacts first, then optionally adding product code.