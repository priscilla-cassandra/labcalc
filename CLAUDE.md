# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

LabCalc is a simple calculator for everyday laboratory calculations, such as dilutions and molarity. Status: in progress.

Tech stack: TypeScript + HTML/CSS, built with Vite (vanilla-ts template, no UI framework).

## Commands

- `npm install` — install dependencies
- `npm run dev` — start the Vite dev server
- `npm run build` — typecheck with `tsc` (no emit) and then build to `dist/`
- `npm run preview` — serve the production build locally
- `npx tsc` — typecheck only

No linter or test runner is set up yet.

## Structure

`index.html` is the entry point and loads `src/main.ts`, which renders into `#app`. The code in `src/` (`main.ts`, `counter.ts`, `style.css`, `assets/`) is still the unmodified Vite starter template and is meant to be replaced with the calculator UI. Static files in `public/` are served from the site root.

`tsconfig.json` makes unused locals and parameters compile errors (note: `"strict"` is not enabled), and uses `verbatimModuleSyntax`, so type-only imports must use `import type`.
