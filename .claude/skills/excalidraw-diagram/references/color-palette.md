# Color Palette & Brand Style

**This is the single source of truth for all colors and brand-specific styles.** To customize diagrams for your own brand, edit this file — everything else in the skill is universal.

> **Constraint: use only the colors listed here.** Every value below is from Excalidraw's stock palette (Open Color). That matters beyond aesthetics: renderers that theme-adapt a drawing — Excalidraw's own dark mode, and the `@quartz-community/obsidian-plugin-excalidraw` used to publish these — only remap colors they recognize. An off-palette color passes through unchanged, so a diagram built from arbitrary hex values looks correct on white and breaks on a dark background. Picking from this file is what makes a diagram theme-safe.

---

## Shape Colors (Semantic)

Colors encode meaning, not decoration. Each semantic purpose has a fill/stroke pair, one per hue so purposes stay visually distinct.

| Semantic Purpose | Fill | Stroke |
|------------------|------|--------|
| Primary/Neutral | `#a5d8ff` | `#1971c2` |
| Secondary | `#99e9f2` | `#0c8599` |
| Tertiary | `#d0bfff` | `#6741d9` |
| Start/Trigger | `#ffd8a8` | `#e8590c` |
| End/Success | `#b2f2bb` | `#2f9e44` |
| Decision | `#ffec99` | `#f08c00` |
| Warning/Reset | `#fcc2d7` | `#c2255c` |
| AI/LLM | `#eebefa` | `#9c36b5` |
| Inactive/Disabled | `#e9ecef` | `#868e96` (use dashed stroke) |
| Error | `#ffc9c9` | `#e03131` |

**Rule**: Always pair a darker stroke with a lighter fill for contrast.

### Hero / emphasis fill

For the single most important shape in a diagram — the visual anchor — invert the usual treatment: a saturated fill with white text, so it reads as the focal point against the pastel fills around it.

| Element | Fill | Stroke | Text |
|---------|------|--------|------|
| Hero shape | `#1971c2` | `#1e1e1e` | `#ffffff` |

Use it once, maybe twice. If everything is a hero, nothing is. Prefer size and whitespace for hierarchy first (see Layout Principles in `SKILL.md`) and reach for this only when scale alone isn't carrying it.

---

## Text Colors (Hierarchy)

Use color on free-floating text to create visual hierarchy without containers.

| Level | Color | Use For |
|-------|-------|---------|
| Title | `#1971c2` | Section headings, major labels |
| Subtitle | `#228be6` | Subheadings, secondary labels |
| Body/Detail | `#868e96` | Descriptions, annotations, metadata |
| Accent | `#f08c00` | The one line per section worth pulling the eye to |
| On light fills | `#1e1e1e` | Text inside light-colored shapes |
| On dark fills | `#ffffff` | Text inside the hero fill |

---

## Evidence Artifact Colors

Used for code snippets, data examples, and other concrete evidence inside technical diagrams.

| Artifact | Background | Text Color |
|----------|-----------|------------|
| Code snippet | `#1e1e1e` | `#b2f2bb` (green), `#a5d8ff` (blue), `#ffec99` (yellow) |
| JSON/data example | `#1e1e1e` | `#b2f2bb` (green) |

Note that `#1e1e1e` inverts to a light background under dark mode, taking its text with it. The pairing stays readable in both themes, but don't expect a code block to look dark on a dark page.

---

## Default Stroke & Line Colors

| Element | Color |
|---------|-------|
| Arrows | Use the stroke color of the source element's semantic purpose |
| Structural lines (dividers, trees, timelines) | `#868e96`, or `#1e1e1e` for a primary spine |
| Marker dots (fill + stroke) | `#1971c2` |

---

## Background

| Property | Value |
|----------|-------|
| Canvas background | `#ffffff` |
