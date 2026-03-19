# Индекс курса

Этот файл нужен как центральная точка входа в курс.
На GitHub он работает как оглавление: отсюда можно быстро перейти к нужному разделу, книге или рабочему документу.

## Как устроен курс

Сейчас курс состоит из нескольких слоев:
- общая рамка и карта курса;
- базовые уроки из первой линии материалов;
- вторая линия уроков, где мы собираем более глубокие и развернутые книги по агентам;
- прикладные playbooks, которые превращают знания в повторяемые сценарии;
- вспомогательные матрицы, программы и рабочие документы.

## Быстрый вход

Если вы открыли репозиторий впервые, лучше идти так:

1. Сначала прочитать главный [README.md](README.md).
2. Затем посмотреть [L1-L10-matrix-simple.md](L1-L10-matrix-simple.md), чтобы понять общую лестницу уровней.
3. Потом перейти к урокам в папке `1_lessons`.
4. После этого перейти к новым углубленным материалам в папке `2_lessons`.
5. Затем выбрать одну из двух развернутых книг: Codex или Claude Code.
6. После базовой книги перейти к прикладным сценариям в [2_lessons/playbooks/README.md](2_lessons/playbooks/README.md).

## Главные файлы верхнего уровня

- [README.md](README.md) — главный вход в курс и общий контекст.
- [L1-L10-matrix-simple.md](L1-L10-matrix-simple.md) — упрощенная карта уровней курса.
- [L3-L8-matrix.md](L3-L8-matrix.md) — более подробная матрица уровней среднего диапазона.
- [course-specification.md](course-specification.md) — спецификация курса.
- [course-program-selling.md](course-program-selling.md) — продающая версия программы.
- [V5_program.md](V5_program.md) — рабочая программа курса.

## Раздел 1. Базовая линия уроков

Папка: `1_lessons`

Это основная существующая линия уроков.
Там лежат отдельные сценарии уроков и сводный файл по диапазону уроков.

Ключевые материалы:
- [lessons-06-28-summary.md](1_lessons/lessons-06-28-summary.md) — обзор и сводка по линии уроков.
- [lesson-01-script.md](1_lessons/lesson-01-script.md) — первый урок.
- [lesson-02-script.md](1_lessons/lesson-02-script.md) — второй урок.
- [lesson-03-script.md](1_lessons/lesson-03-script.md) — третий урок.
- [lesson-04-script.md](1_lessons/lesson-04-script.md) — четвертый урок.
- [lesson-05-script.md](1_lessons/lesson-05-script.md) — пятый урок.

Примечание:
далее в папке продолжается полная последовательность файлов `lesson-06-script.md` и дальше до [lesson-28-script.md](1_lessons/lesson-28-script.md).

## Раздел 2. Новая линия углубленных уроков

Папка: `2_lessons`

Индекс раздела:
- [2_lessons/README.md](2_lessons/README.md)

Это новая линия материалов, где мы строим не короткие конспекты, а более глубокие самодостаточные тексты.

### 2.1. Конспекты учебных траекторий

- [codex-agent-learning-path.md](2_lessons/codex-agent-learning-path.md) — конспект маршрута освоения Codex.
- [claude-code-agent-learning-path.md](2_lessons/claude-code-agent-learning-path.md) — конспект маршрута освоения Claude Code.

### 2.2. Книга по Codex

Папка: `2_lessons/codex-book`

Это развернутая книга по Codex для нетехнической аудитории.
Каждая глава — самостоятельный файл, чтобы материалы не превращались в один неуправляемый документ.

Индекс книги:
- [2_lessons/codex-book/README.md](2_lessons/codex-book/README.md)

Полный состав книги:
- [01-codex-first-contact.md](2_lessons/codex-book/01-codex-first-contact.md) — первое знакомство с Codex, выбор интерфейса и безопасный старт.
- [02-codex-task-design.md](2_lessons/codex-book/02-codex-task-design.md) — постановка задач, рабочий шаблон запроса и режим "сначала план".
- [03-codex-project-memory.md](2_lessons/codex-book/03-codex-project-memory.md) — постоянные инструкции проекта и память агента через `AGENTS.md`.
- [04-codex-settings-and-safety.md](2_lessons/codex-book/04-codex-settings-and-safety.md) — настройки, границы доступа и безопасные режимы работы.
- [05-codex-first-edits-and-checkpoints.md](2_lessons/codex-book/05-codex-first-edits-and-checkpoints.md) — первые правки, точки возврата и проверка изменений.
- [06-codex-repeatable-workflows.md](2_lessons/codex-book/06-codex-repeatable-workflows.md) — repeatable workflows, automation jobs и переход к устойчивым циклам работы.
- [07-codex-autonomy-and-reliability.md](2_lessons/codex-book/07-codex-autonomy-and-reliability.md) — рост автономности и надежности без потери контроля.
- [08-codex-agent-operating-system.md](2_lessons/codex-book/08-codex-agent-operating-system.md) — устройство `Agent Operating System` вокруг Codex.
- [09-codex-agent-organization.md](2_lessons/codex-book/09-codex-agent-organization.md) — переход от одного агента к агентной организации.

Статус раздела:
- текущая базовая линия книги по Codex завершена;
- книга готова как самостоятельный маршрут чтения.

### 2.3. Книга по Claude Code

Папка: `2_lessons/claude-code-book`

Это развернутая книга по Claude Code для нетехнической аудитории.
Каждая глава — самостоятельный файл, чтобы материалы не превращались в один неуправляемый документ.

Индекс книги:
- [2_lessons/claude-code-book/README.md](2_lessons/claude-code-book/README.md)

Полный состав книги:
- [01-claude-code-first-contact.md](2_lessons/claude-code-book/01-claude-code-first-contact.md) — первое знакомство с Claude Code, выбор поверхности работы и безопасный старт.
- [02-claude-code-task-design.md](2_lessons/claude-code-book/02-claude-code-task-design.md) — постановка задач, рабочий шаблон запроса и режим "сначала план".
- [03-claude-code-project-memory.md](2_lessons/claude-code-book/03-claude-code-project-memory.md) — постоянные инструкции проекта, `CLAUDE.md` и auto memory.
- [04-claude-code-settings-and-permissions.md](2_lessons/claude-code-book/04-claude-code-settings-and-permissions.md) — настройки, permission modes и безопасные границы автономности.
- [05-claude-code-first-edits-and-checkpoints.md](2_lessons/claude-code-book/05-claude-code-first-edits-and-checkpoints.md) — первые правки, точки возврата и проверка изменений.
- [06-claude-code-repeatable-workflows.md](2_lessons/claude-code-book/06-claude-code-repeatable-workflows.md) — repeatable workflows, custom commands и регулярные рабочие циклы.
- [07-claude-code-autonomy-and-reliability.md](2_lessons/claude-code-book/07-claude-code-autonomy-and-reliability.md) — рост автономности и надежности без потери контроля.
- [08-claude-code-agent-operating-system.md](2_lessons/claude-code-book/08-claude-code-agent-operating-system.md) — устройство `Agent Operating System` вокруг Claude Code.
- [09-claude-code-agent-organization.md](2_lessons/claude-code-book/09-claude-code-agent-organization.md) — переход от одного агента к агентной организации.

Статус раздела:
- текущая базовая линия книги по Claude Code завершена;
- книга готова как самостоятельный маршрут чтения.

### 2.4. Прикладные playbooks

Папка: `2_lessons/playbooks`

Это набор коротких, но самодостаточных практических сценариев.
Они нужны для того, чтобы брать типовую ситуацию и проходить ее шаг за шагом без восстановления процесса с нуля.

Индекс раздела:
- [2_lessons/playbooks/README.md](2_lessons/playbooks/README.md)

Текущий набор:
- [01-how-to-choose-between-codex-and-claude-code.md](2_lessons/playbooks/01-how-to-choose-between-codex-and-claude-code.md) — как понять, с какого агента лучше начать.
- [02-first-safe-project-review.md](2_lessons/playbooks/02-first-safe-project-review.md) — как безопасно провести первый обзор проекта без изменений файлов.
- [03-first-safe-edit.md](2_lessons/playbooks/03-first-safe-edit.md) — как сделать первую маленькую правку без лишнего риска.
- [04-turn-outline-into-full-chapter.md](2_lessons/playbooks/04-turn-outline-into-full-chapter.md) — как превращать конспект в полноценную главу.
- [05-regular-editorial-pass.md](2_lessons/playbooks/05-regular-editorial-pass.md) — как делать регулярный редакторский проход по уже написанным материалам.

Статус раздела:
- стартовый набор playbooks собран;
- следующий логичный шаг — добавлять более длинные operational scenarios и недельные циклы работы.

## Раздел 3. Справочные документы и матрицы

Эти файлы помогают понимать архитектуру курса, уровни задач и прикладные возможности.

- [017-level-cases-escalation-matrix.md](017-level-cases-escalation-matrix.md)
- [Escalation-matrix.md](Escalation-matrix.md)
- [003-15-benefits-apps-and-automation.md](003-15-benefits-apps-and-automation.md)
- [L9+.md](L9+.md)

## Как читать курс по порядку

Если нужен рекомендуемый маршрут, он сейчас такой:

1. Общий контекст: [README.md](README.md)
2. Карта уровней: [L1-L10-matrix-simple.md](L1-L10-matrix-simple.md)
3. Базовые уроки: папка `1_lessons`
4. Углубленные траектории: папка `2_lessons`
5. Развернутая книга по Codex: [2_lessons/codex-book/README.md](2_lessons/codex-book/README.md)
6. Развернутая книга по Claude Code: [2_lessons/claude-code-book/README.md](2_lessons/claude-code-book/README.md)
7. Прикладные сценарии: [2_lessons/playbooks/README.md](2_lessons/playbooks/README.md)
8. После этого можно сравнивать две среды и выбирать устойчивый рабочий набор под себя.

## Как будет расти структура дальше

Принцип на будущее такой:
- конспект маршрута остается коротким и обзорным;
- полноценные главы выносятся в отдельные файлы;
- на каждый большой раздел появляется свой `README.md` с оглавлением;
- корневой индекс курса обновляется по мере появления новых книг и веток материалов;
- после базовых книг логично добавлять прикладные playbooks, шаблоны и operating packages.
