# claude-ultimate-dev-rules

One `CLAUDE.md` that makes an AI coding assistant **plan first, test first, write minimal code, review strictly, and never touch your secrets.**

## Problems it solves

- The assistant jumps straight into code without understanding the task.
- Over-engineered output (1000 lines for a 100-line job).
- Chatty replies that bury the actions.
- Single-pass reviews that miss security and migration risks.
- Accidental exposure of `.env` files, keys, or customer data.

## 7 Pillars

1. **Planning** — Clarify → Architecture → Tests (TDD) → Minimal code.
2. **Minimal code** — KISS, no needless abstractions or dependencies.
3. **Numbered communication** — no filler, only actions.
4. **Multi-agent review** — virtual sub-agents per domain; main agent verifies every finding in code.
5. **Strict security & code review** — `master...HEAD`, severity-ranked, verdict: `MERGE` / `FIX BEFORE MERGE` / `DO NOT MERGE`.
6. **DB & UI/UX autonomy** — PostgreSQL efficiency, headless-browser checks, design-token fidelity.
7. **Data-leak prevention** — zero-trust rules for secrets, PII, and files outside the project.

## Install

**Claude Code / Desktop** — copy `CLAUDE.md` to your project root. For global use: `~/.claude/CLAUDE.md`.

**Split rules** — put sections into `.claude/rules/*.md` (e.g. `security.md`, `review.md`).

**Cursor / Windsurf** — paste the contents into `.cursorrules` / `.windsurfrules`.

**Enforcement (important)** — copy `.claude/settings.example.json` to `.claude/settings.json`. This blocks reads of secret files at the tool level.

## Honest limits

`CLAUDE.md` is guidance the model follows, not a sandbox. It greatly reduces leaks, but cannot guarantee 100%. Real protection = these rules **plus** `permissions.deny`, secret scanning in CI, and least-privilege credentials.

## License

MIT
