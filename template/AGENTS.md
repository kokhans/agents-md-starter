# [PROJECT_NAME]

[ONE_LINE_DESCRIPTION]

## Overview

- Purpose: [WHAT_PROBLEM_IT_SOLVES_AND_FOR_WHOM]
- Owner: [TEAM_OR_PERSON]
- Stack: [LANGUAGES_AND_VERSIONS], [FRAMEWORKS]

## Project Structure

<!-- Agent: Generate this structure from the repository and keep it current. -->

```text
[DIR]/ [WHAT_LIVES_HERE]
```

## Commands

<!-- Human: Add one bullet per command the agent needs. The verify command runs tests and lint. -->

- `[VERIFY_COMMAND]`: Runs tests and lint.

## Conventions

<!-- Human: Add only rules that differ from language defaults and are not enforced by linters or formatters, and give the reason. -->

- [CONVENTION]: [REASON]

## Security

- Secrets come from [SECRET_SOURCE]. Never print, log, or commit them.
- Never log tokens, passwords, personal data, or full request bodies.
- Never disable authentication, authorization, input validation, or TLS to make a task pass.
- Use the least privilege needed for service accounts, tokens, and CI credentials.
- Never concatenate untrusted input into queries, shell commands, or markup.
- Local, dev, and test environments use fake data and fake credentials, never production values.
- Report suspected vulnerabilities privately to [TEAM_OR_PERSON], not in a public issue.
- Data handling follows [COMPLIANCE_NOTES].

## Version Control

- The agent works on a branch that follows [BRANCH_PATTERN] and never commits directly to the default branch.
- Commits follow [COMMIT_FORMAT] and contain one logical change.
- PRs follow [PR_POLICY] and state what changed and how it was verified.
- The agent never runs `git push`. A developer reviews the agent's commits on the branch and pushes by hand.
- **Never:** edit generated files; force-push or rewrite shared history.
- Never amend, rebase, or squash commits that already exist on a shared branch.

## Testing

- Framework: [TEST_FRAMEWORK].
- Tests live in [TEST_LOCATION] and follow the existing naming and structure.
- New behavior and bug fixes start with a failing test.
- Tests are deterministic and offline, with external services faked at the boundary.
- Cover the failure path as well as the happy path.
- **Never** skip, delete, or weaken tests to make them pass.

## Boundaries

- **Always:** run the verify command before committing; update docs and tests with the change.
- **Ask first:** adding or upgrading dependencies; schema or migration changes; public API changes; authentication or authorization changes; CI/CD or infrastructure config; deleting files or data.
- **Never:** disable, skip, or bypass a check to get a green result.

## Writing Style

- One H1 per file. Headings and subheadings use Title Case.
- Never use em dashes or double dashes in prose. Use a colon, comma, or period.
- Write American English and spell words as Merriam-Webster does: "standardization", "handwritten".
- Put a comma before the last "and" or "or" in a list of three or more items: "print, log, and commit".
- Put a comma after "e.g." and "i.e.".
- Capitalize product names as their owners do: Git, GitHub, macOS, Node.js.
- Bold, not backticks, marks a label at the start of a bullet, with the colon inside the bold: "**Always:**".
- Never use contractions. Write "do not", "does not", "cannot", "is not", "it is", and "you are", not "don't", "doesn't", "can't", "isn't", "it's", and "you're". Possessives such as "the agent's commits" stay.
- Headings use "and", never "&".
- One rule per bullet, in plain present tense: "Server code validates every request." Add the reason only when it is not obvious.
- No introductions, summaries, filler, or motivational text.
- Put packages, files, APIs, commands, flags, and environment variables in backticks.
- Every fenced code block declares a language.
- Links to repository files are relative.
- Comments explain why, not what.
- Keep descriptions short and plain: one sentence in present tense that says what it is or does, not how it works. Do not start with "This function".
- Name Markdown files in lowercase-kebab-case (e.g., `getting-started.md`), except well-known root files that tools look for by name, which stay UPPERCASE with underscores between words (e.g., `README.md`, `AGENTS.md`, `CODE_OF_CONDUCT.md`).

## Gotchas

<!-- Agent: Add an entry every time an agent or a human gets something wrong. -->

- [GOTCHA]

## References

<!-- Human: Point to the reference instead of pasting it, so agents can open it when needed. -->

- Architecture: [docs/architecture.md](docs/architecture.md)
- Glossary: [docs/glossary.md](docs/glossary.md)
- ADRs: [docs/adr/](docs/adr/)

## Agent Instructions

1. **Think before writing.** State assumptions. If a request has several readings, list them and ask instead of picking silently.
2. **Simplicity first.** Write the minimum that solves the task. No speculative features, abstractions, or configurability.
3. **Surgical changes.** Touch only what the task needs and match existing style. Mention unrelated problems; do not fix them unasked.
4. **Goal-driven.** Turn the task into checkable criteria (usually tests). For multi-step work, give a short plan with a check per step.
5. **Report honestly.** Say what you ran, what passed, and what you could not verify.
