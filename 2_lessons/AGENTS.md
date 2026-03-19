# 2 Lessons Instructions

## Scope

These instructions apply to:
- `2_lessons`

## Goal

Build and extend the second line of the course:
- learning paths;
- full books;
- practical playbooks.

This section is for non-technical readers.
The writing style must stay simple, explicit, and practical.

## Audience

- Non-programmers
- Domain experts
- Readers who freeze on unclear interfaces or vague instructions

## Core Writing Rules

- Plain Russian
- Calm, precise tone
- No unnecessary developer slang
- Explain interface actions literally
- Keep books and playbooks self-sufficient
- Prefer one large unit of learning per file

## Parent Layer Note

The repository root `AGENTS.md` is an infrastructure-level file.
It describes framework/runtime orchestration and shared command entry points.

For work inside `2_lessons`, treat that root file as background operational context only.
It is not the source of truth for course authoring, educational structure, audience, or resume logic.

## Autonomy Rules

- Work autonomously by backlog and by the nearest logical next step
- Do not ask intermediate questions
- Pause only on structural forks, instruction conflicts, or real risk of damaging important existing structure
- Update indexes and local readmes without reminders

## Hierarchy Rule

This file is a section-level baseline only.
It must not override more specific local files inside:
- `2_lessons/codex-book`
- `2_lessons/claude-code-book`
- `2_lessons/playbooks`

If a session is opened directly inside a subfolder, the subfolder files are the primary operational layer.

## Session Startup Rule

If a new session starts at the `2_lessons` root, first read:
1. `2_lessons/README.md`
2. `2_lessons/BACKLOG.md`
3. then move into the actual active subfolder and read its local files:
   - `AGENTS.md`
   - `BACKLOG.md`
   - `README.md`
   - handoff files, if they exist there

## Resume Rule

Resume logic should be defined at the active subfolder level, not at the whole `2_lessons` level.
