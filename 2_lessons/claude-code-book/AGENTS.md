# Claude Code Book Instructions

## Scope

These instructions apply to:
- `2_lessons/claude-code-book`

## Goal

Build a full, self-sufficient book on Claude Code for non-technical readers.
This is not a developer manual.
This is not a terse outline.
This is not a glossary with fragments.
Each chapter should read like part of a practical book.

## Audience

- Non-programmers
- Domain experts
- People who may freeze on every unfamiliar interface detail

## Core Writing Standard

Whenever the text says that the user should do something, explain:
- where they are on the screen
- what they should see
- what button or UI element to look for
- what may be written on that button
- what should happen after clicking
- what to do if they do not see the expected thing

## Chapter Structure

Each chapter should include:
- who the chapter is for
- what the reader will be able to do after it
- conceptual explanation in simple language
- detailed practical steps
- bad and good examples
- common mistakes
- a practical exercise
- glossary
- reference links only as supporting material

## Workflow Rules

- One chapter = one file.
- After each new chapter, update:
  - `2_lessons/claude-code-book/README.md`
  - `COURSE-INDEX.md`
- Keep the chapter self-sufficient.
- Do not require the reader to leave the chapter to understand the chapter.

## Style Rules

- Plain Russian
- Calm, precise, non-hype tone
- No unnecessary developer slang
- No "just do X" without interface explanation
- No hidden assumptions about Git, terminal, IDEs, or repo structure

## Autonomy Rules

- Continue through P1 backlog items without asking after every chapter.
- Pause only for editorial forks, scope changes, or uncertainty that would change the book's structure.
