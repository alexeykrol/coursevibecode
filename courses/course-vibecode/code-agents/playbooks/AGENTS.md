# Playbooks Instructions

## Scope

These instructions apply to:
- `education/playbooks`

## Goal

Build self-sufficient practical playbooks for non-technical readers.
Each playbook should help the reader complete one real scenario without needing to reconstruct the process.

## Audience

- Non-programmers
- Domain experts
- Readers who need explicit interface guidance

## Parent Layer Note

This repository does not use a section-level `2_lessons` layer anymore.
For work inside `education/playbooks`, this local file is the primary authoring layer.
Use the repository root [README.md](../README.md) as the upper repo context. (ROADMAP.md lives in the external `essays` repo and is not part of this repository.)

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

If a new session starts directly inside `education/playbooks`, first read:
1. `AGENTS.md`
2. `SESSION-HANDOFF.md`
3. `BACKLOG.md`
4. `README.md`
5. `../../README.md`
6. `../../autonomy/root_docs/ROADMAP.md`

Then resume from the nearest unfinished playbook.

## Autonomy Rule

- Continue by backlog without micro-confirmations
- Update readmes and indexes after meaningful additions
- Pause only on structural forks, conflicts, or real risk
