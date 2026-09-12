# AGENTS.md — reactapp

Context for AI coding agents (Claude Code, Codex, opencode, Cursor, …) working in this repo.
Read this first; keep it current.

## What this is
A small CodeSandbox React demo (`react-buttons-and-tabs`) showcasing styled-components buttons
and tabs. Parked experiment from Jan 2023 — no active development, kept as a reference
playground. Not deployed anywhere.

## Layout
- `src/App.js` — the entire demo (theme map, styled `Button`, tabs).
- `src/index.js` — `ReactDOM.render(<App/>, #root)` entry point (React 16 idiom).
- `src/styles.css`, `public/index.html` — styling and HTML shell.
- `.vs/` — Visual Studio scratch files (editor artifacts, ignored by git history).

## Commands
```bash
npm install      # deps: react/react-dom 16.12, react-scripts 3.0.1, styled-components 5
npm start        # dev server (react-scripts start)
npm run build    # production build
npm test         # react-scripts test --env=jsdom
```
No lint script is configured.

## Conventions
- Create React App (react-scripts 3.x) + styled-components; no TypeScript in use despite the
  TS devDependency.
- Default branch is `main`. Feature branch → PR; never push directly to `main`.
- No CI workflows. No lockfile committed — respect the pinned versions in `package.json`.

## Gotchas
- Downgrade/upgrade caution: react-scripts 3.x targets Node ≤14 era tooling; newer Node may
  need `NODE_OPTIONS=--openssl-legacy-provider` or a react-scripts bump to build.
- Uses the React 16 `ReactDOM.render` API — switching to React 18 requires `createRoot`.
