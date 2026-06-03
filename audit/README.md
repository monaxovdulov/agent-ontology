# Content Audit: AI Agents Taxonomy

## Цель

Этот аудит фиксирует, почему текущий `index.html` пока не готов как самостоятельная public-facing taxonomy перед большой переработкой. Аудит не меняет страницу, дизайн или HTML. Он оценивает текст как аргументированную карту: читатель должен понимать, какие claims делает страница, какие источники их поддерживают, где есть reasoning bridge и где вывод является осторожной taxonomy decision, а не уверенной opinion.

## Что проверялось

- `README.md`
- `index.html`
- `research/README.md`
- `research/sources.md`
- `research/candidates-for-page.md`
- `research/content-risks.md`
- `research/negative-findings.md`
- `research/rejected.md`
- `tasks/*.md`

## Критерии

- **Evidence:** источник должен действительно поддерживать claim, а не просто быть по теме.
- **Logic:** нужен явный переход `source evidence -> reasoning -> taxonomy decision`.
- **Reader trust:** страница не должна звучать как changelog, internal critique или task completion report.
- **Taxonomy clarity:** определения, оси, уровни, роли, паттерны, протоколы и продукты не должны смешиваться.
- **Freshness:** claims про продукты, протоколы и 2026-status должны быть датированы и привязаны к living docs/specs.

## Evidence scale

- **strong:** claim напрямую поддержан primary source/spec/paper и не требует широкой inference.
- **medium:** источники поддерживают направление, но wording требует осторожности или reasoning bridge.
- **weak:** источник тематически близок, но claim в текущей формулировке выводится с заметной inference.
- **contested:** research backlog прямо предупреждает о смешанных или недостаточных public signals.
- **missing:** в просмотренном research backlog нет достаточной поддержки.

## Главный диагноз

Текущая страница полезна как внутренний repair log и rough taxonomy draft, но слаба как публичный reader-facing документ. Она часто говорит о том, что было неверно "в исходнике", вместо того чтобы строить доказательную карту с локальными evidence annotations. Сильные идеи есть: разделение autonomy/topology/coordination, workflow-vs-agent, protocol layer, memory boundaries, eval-driven architecture. Но многие формулировки звучат слишком окончательно: "канонический", "де-факто стандарт", "атом всех систем", "80% production", "MCP сильнее", "A2A enterprise-нишевый", "evaluation выбирает архитектуру".

## Verdict

Как public taxonomy текущая страница готова примерно на **45-55%**. Каркас есть, но до сильного rewrite нужно:

1. Перенести meta/changelog в appendix или hidden notes.
2. Переписать спорные claims в date-stamped, source-backed taxonomy decisions.
3. Добавить скрытую локальную annotation system для claims.
4. Заменить footer-only bibliography на claim-linked evidence.
5. Пересобрать порядок аргументации вокруг evidence -> reasoning -> taxonomy decision.
