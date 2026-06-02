# Agent Ontology

Static GitHub Pages project for the AI agents taxonomy page:

https://monaxovdulov.github.io/agent-ontology/

## Structure

- `index.html` — published page and GitHub Pages entry point.
- `assets/styles.css` — visual styles extracted from the original single-file page.
- `agent-ontology.html` — legacy redirect to the repository root.
- `tasks/` — source notes and follow-up task documents.

The project intentionally has no framework, build step, or npm dependencies. Moving the long-form content to Markdown should be done as a separate step with either GitHub Pages/Jekyll layouts or a committed pre-rendered HTML workflow, so the root `index.html` remains the served page.
