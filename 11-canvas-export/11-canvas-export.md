---
up: "[[HOME|home]]"
---

# Canvas Export

**Command:** `Breadcrumbs: Export to canvas`

Demonstrates two canvas fixes:

- **Semantic edge anchors** (#782): an opt-in toggle that anchors edges by field group instead of by layout direction.
- **Stale group fields** (#781): export follows every field in the selected groups, resolved at export time.

## Structure demonstrated

| Hub's field | Neighbour | Group | Semantic anchor |
|---|---|---|---|
| `up` | Portfolio | ups | top → bottom |
| `down` | Design, Build | downs | bottom → top |
| `next` | Phase 2 | nexts | right → left |
| `tomorrow` | Tomorrow | nexts (custom field) | right → left |
| `prev` | Phase 0 | prevs | left → right |
| `same` | Twin | sames | left → right |
| — | Sibling | sames | left → right. Links to Hub **only** via its own `same` (the #781 case) |

## Try it

1. Open **[[Hub]]**.
2. Run **Breadcrumbs: Export to canvas**.
3. Select **all** field groups, set **Depth** to `1`, and turn on **Semantic edge anchors**.
4. Click **Create canvas**, and compare it with the pre-built pair below.

| Canvas | Semantic anchors |
|---|---|
| [[Hub canvas - default.canvas]] | off: every edge is right → left (the old behavior) |
| [[Hub canvas - semantic.canvas]] | on: ups top, downs bottom, nexts right, prevs/sames left |

In the semantic canvas, drag **Portfolio** above Hub and **Design**/**Build** below it: the edges snap into a clean vertical structure.

Fields outside the default groups keep the direction default (right → left).

> **Known issue (#785):** both canvases show a `same` edge from Hub to itself. That's the **self is sibling** setting (on by default for `same`), which adds a self-loop so a note appears in its own sibling list in the views. The canvas export doesn't filter it out yet.
