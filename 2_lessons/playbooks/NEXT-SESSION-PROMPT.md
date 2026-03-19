# Prompt For Next Playbooks Session

Use this exact prompt in the next session if you open it inside `2_lessons/playbooks`:

```text
Работай в /Users/alexeykrolmini/Code/coursevibecode/2_lessons/playbooks.

Сначала прочитай по порядку:
1. AGENTS.md
2. SESSION-HANDOFF.md
3. BACKLOG.md
4. README.md
5. ../AGENTS.md
6. ../BACKLOG.md
7. ../README.md

Считай, что корневой AGENTS.md проекта относится только к framework/runtime и не управляет логикой написания курса в этой папке.
Главный рабочий слой для этой сессии — локальные инструкции папки playbooks и section-level инструкции папки 2_lessons.

После чтения не пересказывай лишнее.
Сразу восстанови рабочий контекст и продолжай автономно по backlog.
Не задавай промежуточных вопросов.
Останавливайся только при структурной развилке, конфликте инструкций или риске повредить важную существующую структуру.

Работай в ветке:
codex/2-lessons-session-reset

Текущая точка продолжения:
06-weekly-content-production-cycle.md

После него продолжай без паузы:
07-building-project-instructions.md
08-safe-growth-of-autonomy.md
09-agent-organization-for-small-team.md
```
