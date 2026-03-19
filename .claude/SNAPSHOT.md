# SNAPSHOT — coursevibecode

*Last updated: 2026-03-18*

## Current State

**Version:** 1.22
**Status:** `2_lessons` current content line complete and stabilized
**Branch:** `codex/2-lessons-session-reset`

## Project Overview

`coursevibecode` is a markdown-first course repository for non-technical readers who want to move from ordinary AI chats toward structured work with agent tools.

The active development line is `2_lessons/`, where the repository now holds:
- two short learning-path outlines;
- a practical comparison guide for Codex and Claude Code;
- a full book on Codex;
- a full book on Claude Code;
- a first full set of practical playbooks `01`-`09`.

## Current Structure

```text
coursevibecode/
├── README.md
├── COURSE-INDEX.md
├── CHANGELOG.md
├── 2_lessons/
│   ├── README.md
│   ├── AGENTS.md
│   ├── BACKLOG.md
│   ├── SESSION-HANDOFF.md
│   ├── codex-agent-learning-path.md
│   ├── claude-code-agent-learning-path.md
│   ├── codex-vs-claude-code-in-practice.md
│   ├── codex-book/
│   ├── claude-code-book/
│   └── playbooks/
├── .claude/
├── .codex/
└── src/framework-core/
```

## Recent Progress

- [x] Added a global `COURSE-INDEX.md` and a section index for `2_lessons/`
- [x] Built `2_lessons/codex-book` chapters `01`-`09`
- [x] Built `2_lessons/claude-code-book` chapters `01`-`09`
- [x] Added both learning-path outline files for Codex and Claude Code
- [x] Added playbooks wave 1: `01`-`05`
- [x] Added playbooks wave 2: `06`-`09`
- [x] Ran an editorial and terminology pass across playbooks `01`-`09`
- [x] Aligned playbooks `06`-`09` with the matching chapters in both books
- [x] Added `2_lessons/codex-vs-claude-code-in-practice.md` as a separate practical comparison guide
- [x] Decided not to add a separate templates/prompts layer yet
- [x] Added section-level handoff and next-session files for reset-safe continuation
- [x] Corrected `AGENTS.md` hierarchy so local course-writing files override framework background guidance
- [x] Refreshed section indexes and root navigation for the full playbooks set

## Active Work

- [ ] Keep watching for repeated prompt/template patterns that might later justify a separate layer
- [ ] Decide what the next substantive expansion after the stabilized `2_lessons` line should be

## Next Steps

- [ ] Only create a templates/prompts layer if repeated patterns become substantial across multiple guides
- [ ] Re-check playbooks `01`-`05` only if the next real new artifact introduces fresh wording drift
- [ ] Decide what the next non-artificial expansion should be

## Key Concepts

- The audience is non-technical and needs literal interface guidance.
- Full lessons must be self-sufficient, not just link collections.
- `AGENTS.md` + `BACKLOG.md` + handoff files form the operating layer for long work.
- Autonomy depends on configuration, explicit artifacts, and fresh session context.
- Root framework memory lives in `.claude/`; section-specific resume logic lives closer to the active folder.

---
*Primary root-level context for the next session. Pair with `.claude/SESSION-HANDOFF.md` when resuming after a reset.*
