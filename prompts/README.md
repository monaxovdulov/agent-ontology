# Rewrite Prompt Queue

Эта папка содержит indexed prompts для последовательной переработки страницы AI agents taxonomy после аудита.

## Как запускать в новой сессии

В новой сессии достаточно сказать агенту:

```text
Ты работаешь в репозитории C:\Users\user\Desktop\agent-ontology.
Прочитай prompts/README.md, prompts/index.md и prompts/progress.md.
Выполни следующую задачу со статусом [ ] из prompts/progress.md.
Не переходи к следующей задаче. После завершения обнови prompts/progress.md.
```

Если нужна конкретная задача, скажи:

```text
Ты работаешь в репозитории C:\Users\user\Desktop\agent-ontology.
Выполни prompts/06-protocol-stack-mcp-a2a.md.
```

## Общие правила для всех задач

- Сначала читать `audit/README.md`, `audit/priority-fixes.md` и релевантные части `audit/claim-ledger.md`.
- Использовать `research/` как основной источник evidence.
- Не добавлять новые внешние источники без необходимости; сначала использовать `research/sources.md`, `research/content-risks.md`, `research/negative-findings.md`.
- Отличать documented source evidence от taxonomy inference.
- Учитывать, что исследования, specs, продукты, safety guidance и benchmarks регулярно меняются: living/current claims должны иметь review/access date, а новые источники сначала добавляются в `research/` и evidence registry с указанием, какой claim они поддерживают, ограничивают или оспаривают.
- После задачи обновлять `prompts/progress.md`: отметить done, коротко записать что изменено и какие проверки выполнены.
- После обновления progress делать scoped git commit с результатом задачи и handoff-правилом, если репозиторий доступен. Коммит должен включать только нужные для задачи файлы и оставлять следующую задачу со статусом `[ ]`.
- Не делать следующую задачу без явного запроса пользователя.
- Если редактируется `index.html`, сохранять текущую визуальную систему и не превращать страницу в academic paper с квадратными citation markers.

## Definition of done для каждой задачи

- Изменения scoped только к prompt.
- Нет новых unsupported strong claims.
- Спорные формулировки либо смягчены, либо снабжены annotation/evidence.
- Time-sensitive claims имеют дату review/access; если новые исследования меняют evidence strength, это отражено в source notes или оставлено как явный residual risk.
- `index.html` остаётся валидным single static page.
- В финальном ответе агент перечисляет файлы, проверки и оставшиеся риски.
