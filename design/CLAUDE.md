# Design phase rules (Figma, UAE DS 4.0)

Always-on core. Details are in the `uae-ds4-toolkit` plugin skills: `redesign-page`
(workflow), `figma-build-rules`, `aegov-card`, `capture-reference`,
`figma-file-organisation`, `qa-check`, `inner-page-layouts`, `page-from-content`,
`ds4-library` (keys, mapping, aegov MCP usage). Load the relevant skill before acting.
Project facts are in `../CLAUDE.md`; page decisions in `../DECISIONS.md`.

## Core rules
- DESIGN ONLY, no code. Use the aegov MCP for guidance only (see `ds4-library`).
- Use 4.0 library instances, variables and text styles. No hardcoded colours, spacing or
  fonts. No detached instances. Never hand-draw what the library has.
- Set the project's brand colour mode on every top-level frame you create.
- Layout frames have NO fill (`fills = []` in the same script that creates them).
- Custom boxes: `Container / <Name>`, every value bound to DLS variables, WCAG AA.
- Copy 100% of the live (or supplied) content. Never invent text or translations.
- If no 4.0 component exists for something, do not invent one: ask (Open items).
- Desktop (1536) EN only until approved. Tablet, Mobile, Arabic RTL only when asked.
- Never edit frames you were not asked to touch. Changes go on a copy
  `<name> (v2 ...)`. Never delete originals, components or loose nodes.
- Check the project's Component registry before building anything new; update it in the
  same turn when a component changes, and tell the user.
- Do not edit the shared library unless asked; report any library edit.

## Approval gates
Plan first → wait for OK → build → one screenshot + `qa-check` → STOP and wait.
Many-instance changes: one pilot, screenshot, wait for OK. Batch feedback before edits.
After each page, propose learned rules and wait for OK before adding them.

## Credit-saving
One page per request. Reuse outlines and screenshots; don't re-read the live site. Use
library keys instead of broad searches. Metadata on one frame, never a whole page.
Screenshots only at checkpoints. Ask before anything large or repeated.

## EHS
Brand mode: `EHSblue`. Banner: project skill `sub-page-banner`. Decisions: `../DECISIONS.md`.
