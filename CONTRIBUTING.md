# Contributing

## Non-negotiable

1. **Never weaken Section A (Red Line).** PRs that loosen data-privacy rules are rejected.
2. **Never include real secrets, company data, or PII** in rules, examples, issues, or PRs. Use `<REDACTED>` and fake data.
3. Found a gap that could leak data? Report privately via the repo's Security Advisory, not a public issue.

## How to contribute

1. Open an issue: the problem, an example prompt where the rule failed.
2. Branch from `main`: `feat/<topic>` or `fix/<topic>`.
3. Change one section per PR.
4. Keep rules: short, numbered, testable, imperative.
5. Run the checklist below, then open the PR.

## PR checklist

1. Rule is concrete (a reviewer can say pass/fail).
2. No duplicate of an existing rule.
3. Does not conflict with precedence order at the top of `CLAUDE.md`.
4. Tested on at least one real task; paste before/after behavior (no secrets).
5. README updated if a pillar changed.

## Style

- English, imperative voice.
- No filler, no marketing words.
- Prefer deleting a rule over adding a vague one.

## License

Contributions are MIT-licensed.
