# Repository Instructions

## Scope

- This is a Markdown-only MBA knowledge base containing 16 course-specific agent skills, not an application or package.
- No manifest, lockfile, CI workflow, task runner, build, test, lint, formatter, typecheck, or codegen configuration exists at the repository root. Do not invent install or verification commands.

## Skill Layout

- `.claude/skills/` and `.agents/skills/` are parallel copies of the same skill corpus. Keep both trees synchronized when changing a skill.
- Each skill directory contains `SKILL.md`, `chapters/`, `cheatsheet.md`, `glossary.md`, and `patterns.md`.
- Treat directory names and `SKILL.md` frontmatter `name` values as stable skill IDs. If an ID is intentionally corrected, rename it in both mirrors and update all links and references.
- Read the relevant `SKILL.md` first. It is the entrypoint and index; use `chapters/` for detailed treatments and the supporting files for quick lookup and reusable procedures.
- If a chapter or supporting file is added, removed, or renamed, update the corresponding links and indexes in `SKILL.md` in both trees.

## Verification

- After editing a skill, verify the mirrors remain identical with `diff -rq .claude/skills .agents/skills`.
- Preserve the scope limits in each skill: these are textbook syntheses and do not replace current legal, regulatory, statistical, accounting, or other professional guidance.
