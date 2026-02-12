# Помощь по Claude Export

## Что это такое?

Claude Export — утилита для экспорта диалогов Claude Code в Markdown формат с управлением видимостью в Git.

## Основные функции

### Автоматический экспорт
- Диалоги автоматически экспортируются в папку `.dialog/`
- Обновления происходят в реальном времени

### Управление видимостью
- **Public** — диалог будет включён в git commit
- **Private** — диалог добавлен в `.gitignore`

### Поиск
Используйте поле поиска для фильтрации диалогов по содержимому саммари.

## Горячие клавиши

- `Escape` — закрыть это окно

## Структура файлов

```
.dialog/
├── 2025-12-05_session-abc123.md
├── 2025-12-05_session-def456.md
└── ...
```

## Ссылки

- [GitHub Repository](https://github.com/anthropics/claude-export)
- [Документация](https://github.com/anthropics/claude-export#readme)

---

*Claude Export v2.1.0*
