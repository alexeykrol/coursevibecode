# Playbooks Instructions

## Scope

These instructions apply to:
- `2_lessons/playbooks`

## Goal

Build self-sufficient practical playbooks for non-technical readers.
Each playbook should help the reader complete one real scenario without needing to reconstruct the process.

## Audience

- Non-programmers
- Domain experts
- Readers who need explicit interface guidance

## Parent Layer Note

The repository root `AGENTS.md` is infrastructure-only.
The `2_lessons/AGENTS.md` file is the section-level baseline.

For work inside `2_lessons/playbooks`, this local file is the primary authoring layer.
If there is any tension between generic infrastructure guidance and course-writing guidance, follow the course-writing guidance here.

## Writing Rules

- Plain Russian
- Calm, precise tone
- One playbook = one scenario
- Explain interface actions literally
- When useful, separate steps for Codex and Claude Code
- Prefer practical action over abstract theory

## Structure

Each playbook should include:
- who it is for
- when to use it
- what result the reader should expect
- preparation
- detailed steps
- examples of prompts
- common mistakes
- exercise
- glossary
- source links as supporting material

## Session Startup Rule

If a new session starts directly inside `2_lessons/playbooks`, first read:
1. `AGENTS.md`
2. `SESSION-HANDOFF.md`
3. `BACKLOG.md`
4. `README.md`
5. `../AGENTS.md`
6. `../BACKLOG.md`
7. `../README.md`

Then resume from the nearest unfinished playbook.

## Autonomy Rule

- Continue by backlog without micro-confirmations
- Update readmes and indexes after meaningful additions
- Pause only on structural forks, conflicts, or real risk
