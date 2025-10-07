# Contributing

## Branching
- Создавай ветки от `main`.
- Именование: `feature/TASK-123-short-description`, `fix/bug-short-desc`, `hotfix/urgent-...`.
- Максимальная продолжительность feature branch: 1-2 дня.

## Pull Request process
1. Создал ветку → сделал коммиты (atomic, понятные сообщения).
2. Открыл PR: в описании — что сделано, как протестировать, связанные таски.
3. CI должен быть зелёным.
4. Минимум 1–2 review approvals (зависит от размера команды).
5. Merge через squash or merge — команда выбирает формат.
6. После merge — ветка удаляется.

## Коммиты
Структура: `type(scope): short description`
Примеры: `feat(auth): add jwt login`, `fix(api): handle 500 on timeout`

## Частые команды
- `git checkout -b feature/TASK-123-short-desc`
- `git rebase main` (если нужно обновить ветку)
