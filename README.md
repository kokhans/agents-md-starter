# agents-md-starter

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Open-source, stack-agnostic starter kit that provides any kind of project, MVP, PoC, or spike with a standard `AGENTS.md` and supporting docs for AI-assisted development.

> A coding agent works well only when it knows what the project is, where the code lives, how to verify a change, and what must never be touched. This starter supplies that context and leaves the project process to the humans who own it.

## Why

Every existing or new project starts with another handwritten `AGENTS.md`. Each rewrite varies in structure, wording, and quality, which weakens support, extensibility, standardization, and correctness. One maintained template keeps agent instructions consistent and reviewable across projects.

## Agent Context, Not Project Process

The template covers what the system is and how to change it. It does not cover how the team plans, tracks, or ships work.

| In the template (agent context)           | Out of the template (SDLC)                |
| ----------------------------------------- | ----------------------------------------- |
| Stack, structure, and commands            | Sprints, planning sessions, and estimates |
| Conventions that linters do not enforce   | Ticket workflow and status reports        |
| Verify, test, and review rules            | Release planning and delivery dates       |
| Security, boundaries, and version control | Roadmaps and prioritization               |

## Getting Started

### New Project?

Copy `template/` into a new project without the Git history of this repository.

> [!IMPORTANT]
> Node.js is required to run `degit`. Install the current LTS release from [nodejs.org](https://nodejs.org/) if `npx` is not available.

```sh
npx degit kokhans/agents-md-starter/template my-project
cd my-project
```

### Existing Project?

Clone the starter repository once and keep it outside your project. It is only a source for the template.

```sh
git clone --depth 1 https://github.com/kokhans/agents-md-starter.git
```

Copy the contents of `template/` into your repository root. The copy adds an `AGENTS.md` file and a `docs/` folder, and it leaves your other files untouched.

> [!CAUTION]
> Check for collisions first. Your project may already have `AGENTS.md` or a `docs/` folder with files of the same name. Merge the template into existing files instead of overwriting them.

On macOS, WSL, and Git Bash:

```sh
cp -r agents-md-starter/template/. /path/to/your-project/
```

On Windows PowerShell:

```powershell
Copy-Item -Recurse agents-md-starter/template/* C:\path\to\your-project
```

### Make It Yours

1. Fill in every `[UPPER_SNAKE_CASE]` placeholder with the details of your project.
2. Delete the HTML comments once their instructions are applied.
3. Commit `AGENTS.md` and `docs/` together with the first change that uses them.

## Template Structure

```text
template/                           Starter kit copied into your repository
  AGENTS.md                         Entry point agents read before working
  docs/architecture.md              How the system is built and where its boundaries are
  docs/glossary.md                  Project terms defined once
  docs/adr/0000-adr-template.md     Format for recorded architecture decisions
```

## Design Principles

- **Agent context first:** Every section answers a question that an agent asks before or during a change.
- **Small by default:** The `AGENTS.md` file stays under 150 lines unfilled.
- **Stack-agnostic:** The template assumes no language, framework, package manager, or cloud.
- **One source of truth:** The `AGENTS.md` file summarizes and links, and `docs/` holds the detail.
- **Explicit ownership:** Comments starting with `Agent:` mark work for the agent, and comments starting with `Human:` need a person.
- **Checkable rules:** Every rule is specific enough to verify.

## License

The project is licensed under the [MIT License](LICENSE).
