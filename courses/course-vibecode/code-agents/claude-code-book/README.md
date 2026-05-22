# Книга по Claude Code

Это оглавление развернутой книги по освоению Claude Code для нетехнической аудитории.

Принцип структуры такой:
- конспект маршрута лежит отдельно;
- полная книга собирается отдельными главами;
- каждая глава самодостаточна и посвящена одному большому шагу освоения;
- читатель должен получать основное понимание внутри главы, а не через беготню по внешним ссылкам.

## Кейсы: какую главу читать

- Если вы пока не понимаете, что такое `Claude Code`, где он работает и как безопасно сделать первую сессию, начните с [01-claude-code-first-contact.md](01-claude-code-first-contact.md).
- Если агент в `Claude Code` угадывает лишнее и вы хотите научиться ставить задачи так, чтобы он не фантазировал, читайте [02-claude-code-task-design.md](02-claude-code-task-design.md).
- Если вам нужно понять, как работают `CLAUDE.md`, auto memory и постоянные инструкции проекта, откройте [03-claude-code-project-memory.md](03-claude-code-project-memory.md).
- Если вы упираетесь в permission modes, настройки и безопасные границы, вам нужен [04-claude-code-settings-and-permissions.md](04-claude-code-settings-and-permissions.md).
- Если вы готовы к первой реальной правке, но хотите пройти ее через diff, checkpoints и безопасную проверку, идите в [05-claude-code-first-edits-and-checkpoints.md](05-claude-code-first-edits-and-checkpoints.md).
- Если у вас бывают хорошие сессии, но нет устойчивого workflow, читайте [06-claude-code-repeatable-workflows.md](06-claude-code-repeatable-workflows.md).
- Если вы хотите повысить автономность `Claude Code`, но не потерять контроль, нужен [07-claude-code-autonomy-and-reliability.md](07-claude-code-autonomy-and-reliability.md).
- Если вы уже проектируете operating layer вокруг агента, переходите к [08-claude-code-agent-operating-system.md](08-claude-code-agent-operating-system.md).
- Если вы хотите вырасти от одного агента к командной системе ролей и делегирования, читайте [09-claude-code-agent-organization.md](09-claude-code-agent-organization.md).
- Если вы поддерживаете сам раздел и хотите быстро понять writing contract книги, используйте [AGENTS.md](AGENTS.md).
- Если вы развиваете книгу и хотите увидеть текущий editorial backlog, откройте [BACKLOG.md](BACKLOG.md).

## Входные материалы

- [Конспект маршрута освоения Claude Code](../root_docs/claude-code-agent-learning-path.md)
- [Отдельный практический guide по интерфейсам Claude Code](../root_docs/claude_code_interfaces.md)
- [Индекс репозитория code-agents](../README.md)

## Текущий статус

Текущая базовая книга по Claude Code собрана полностью.
Она покрывает весь путь:
- от первого знакомства с агентом;
- до постановки задач, памяти проекта, настроек и первых правок;
- затем до repeatable workflows, управляемой автономности, `Agent Operating System` и агентной организации.

## Главы

1. [01-claude-code-first-contact.md](01-claude-code-first-contact.md) — что такое Claude Code, где он работает, как безопасно начать и как провести первую сессию без риска.
2. [02-claude-code-task-design.md](02-claude-code-task-design.md) — как ставить задачи Claude Code так, чтобы он не угадывал лишнего, и как пользоваться простым шаблоном рабочего запроса.
3. [03-claude-code-project-memory.md](03-claude-code-project-memory.md) — как устроены постоянные инструкции проекта, что хранить в `CLAUDE.md` и как работает auto memory.
4. [04-claude-code-settings-and-permissions.md](04-claude-code-settings-and-permissions.md) — какие настройки реально важны, как понимать permission modes и где проходят безопасные границы автономности.
5. [05-claude-code-first-edits-and-checkpoints.md](05-claude-code-first-edits-and-checkpoints.md) — как делать первые правки, создавать точки возврата, смотреть diff и принимать только полезную часть результата.
6. [06-claude-code-repeatable-workflows.md](06-claude-code-repeatable-workflows.md) — как перейти от удачных разовых запросов к повторяемым рабочим процессам и когда уместны custom commands, recurring tasks и автоматизация.
7. [07-claude-code-autonomy-and-reliability.md](07-claude-code-autonomy-and-reliability.md) — как повышать автономность по ступеням, не теряя надежность, границы и контроль качества.
8. [08-claude-code-agent-operating-system.md](08-claude-code-agent-operating-system.md) — что такое `Agent Operating System`, из каких слоев он собирается в Claude Code и как устроены `runtime baseline`, `project overlay` и `preflight`.
9. [09-claude-code-agent-organization.md](09-claude-code-agent-organization.md) — как из работы с одним Claude Code вырастает система ролей, делегирования, общей памяти и организационной агентности.

## Как читать книгу по порядку

Если вы начинаете с нуля, идите так:
1. главы 1-2 — вход и постановка задач;
2. главы 3-5 — память проекта, настройки, первые изменения и проверка;
3. главы 6-7 — repeatable workflows, автономность и надежность;
4. главы 8-9 — `Agent Operating System` и агентная организация.

## Что делать после этой книги

После этой линии логично идти в одну из трех сторон:
1. сделать редакторский проход и улучшить существующие главы;
2. читать параллельную книгу по Codex и сравнить две рабочие среды;
3. собирать практические шаблоны, operating packages и рабочие сценарии под реальные проекты.

## Companion guide

Если после книги нужен не следующий большой этап, а короткий справочник именно по тому, чем отличаются CLI, VS Code Extension и Desktop App, используйте:

- [../claude_code_interfaces.md](../root_docs/claude_code_interfaces.md)
