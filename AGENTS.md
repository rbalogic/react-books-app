# AI Agent Instructions (Codex, Gemini, etc.)

Reusable project instructions for AI agents working in this repository.

## Project Snapshot

- App: `react-books-app` (Create React App, React 16)
- Package manager: `npm`
- Frontend dev server: `http://localhost:3000`
- API dependency: `http://localhost:4000` (expects endpoints like `/books` and `/categories`)

## Runtime Requirements

- Use Node.js LTS (`18` or `20` recommended).
- Avoid Node.js `24+` for this codebase; old CRA dependencies may fail with runtime errors (for example `No such module: http_parser`).

## Setup

From repository root:

```bash
nvm use 20 || nvm use 18
npm install
```

If dependencies were installed under an incompatible Node version:

```bash
rm -rf node_modules package-lock.json
npm install
```

## Run Commands

- Start frontend: `npm start`
- Build production assets: `npm run build`
- Run tests: `npm test`

## Backend Requirement

Before validating UI data rendering, ensure API server is running on port `4000`.

Quick check:

```bash
curl http://localhost:4000/books
```

If this fails, frontend may show `Failed to fetch`.

## Working Rules For Agents

- Keep changes focused on the requested task only.
- Preserve existing coding style in touched files.
- Avoid broad dependency upgrades unless explicitly requested.
- Do not commit or push unless the user explicitly asks.
- Do not run destructive git commands.

## Validation Before Handover

For code changes, run:

```bash
npm test -- --watch=false
```

If tests are not practical in the current environment, report what was run and what remains.
