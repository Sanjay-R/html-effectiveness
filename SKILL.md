---
name: html-communication
description: Creates a polished, potentially interactive single HTML page or explicitly requested linked multi-page static HTML collection to communicate an idea, comparison, plan, review, report, diagram, explainer, prototype, or editing workflow. Use when the user asks for a styled HTML artifact, visual communication site, interactive explanation, or presentation based on the html-effectiveness gallery.
license: Apache-2.0
---

# HTML Communication

Create a useful static HTML artifact from the user's request and current context. Default to one standalone page; create a linked multi-page collection only when the user asks for one.

## Source

The offline source templates are in `templates/` relative to this `SKILL.md`.

Read `templates/README.md` and `templates/index.html` only when routing is unclear. Then read the selected numbered HTML file completely. Do not read all examples.

## Choose exactly one primary structure

1. `01-exploration-code-approaches.html` — compare implementation approaches and trade-offs.
2. `02-exploration-visual-designs.html` — compare visual/layout directions.
3. `03-code-review-pr.html` — annotated review findings, severity, and navigation.
4. `04-code-understanding.html` — module map, call flow, entry points, and hot path.
5. `05-design-system.html` — tokens, typography, spacing, and reusable visual rules.
6. `06-component-variants.html` — component states, sizes, and variants.
7. `07-prototype-animation.html` — tune motion, timing, and easing interactively.
8. `08-prototype-interaction.html` — clickable multi-step interaction flow.
9. `09-slide-deck.html` — concise arrow-key presentation.
10. `10-svg-illustrations.html` — a sheet of editable inline SVG figures.
11. `11-status-report.html` — progress, metrics, shipped/slipped work, and blockers.
12. `12-incident-report.html` — incident timeline, evidence, impact, and follow-ups.
13. `13-flowchart-diagram.html` — annotated process or decision flowchart.
14. `14-research-feature-explainer.html` — explain how a concrete feature works.
15. `15-research-concept-explainer.html` — teach a general concept interactively.
16. `16-implementation-plan.html` — milestones, flow, risks, decisions, and handoff.
17. `17-pr-writeup.html` — motivation, before/after, file tour, tests, and review focus.
18. `18-editor-triage-board.html` — drag/reorder/categorize items, then export.
19. `19-editor-feature-flags.html` — edit toggles with dependency warnings and export a diff.
20. `20-editor-prompt-tuner.html` — edit a template and preview sample renderings live.

Pick the structure that reduces the reader's cognitive work, not the prettiest template. If two fit, use the simpler one. For a collection, use one coherent visual language and select the most applicable structure for each page; do not force every page into the same layout. State the selections only in the final response, not as a decision essay.

## Output mode

- **Single page (default):** one self-contained `.html` file.
- **Multi-page (only when requested):** one directory containing `index.html` plus a minimal set of clearly named linked pages. Add consistent primary navigation, mark the current page, provide a route back to the index, and use relative links so the collection works from disk or any static host. Use a shared local stylesheet when that avoids substantial duplication; use shared JavaScript only when behavior is genuinely shared.

## Build

1. Gather facts from the current conversation and relevant local files/tools. Do not invent project facts; visibly label unknowns.
2. Adapt the selected source file or files rather than designing a new system.
3. Replace all fictional sample content. Keep useful layout, CSS, inline SVG, and minimal interaction patterns.
4. Use HTML, CSS, inline SVG, and plain JavaScript only. No build step, package, framework, CDN, web font, analytics, or remote asset. A single page must remain one self-contained file; a collection may use local shared assets.
5. Keep interaction only when it improves understanding. Provide keyboard operation, visible focus, semantic HTML, and reduced-motion behavior where applicable.
6. Make it responsive and readable when printed when the artifact type benefits from printing.
7. Retain the upstream copyright/SPDX comment. Add a nearby comment that the file was adapted and modified when source code is copied.
8. Write to the path requested by the user. Otherwise use a short descriptive filename for a single page or directory name for a collection in the current working directory.
9. Check the result with the cheapest relevant checks: verify titles and viewports, no remote dependencies, core tag balance, and JavaScript syntax when non-trivial. For a collection, also verify every local link target exists and every page links back into the collection.

Do not create a generator, framework, reusable component layer, or documentation unless explicitly requested.

## Result

Reply with:

- the output file or collection index path;
- the chosen numbered structure(s) and why they fit, in one sentence;
- any material unknowns or intentionally omitted interaction.