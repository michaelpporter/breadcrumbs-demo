---
up: "[[HOME|home]]"
BC-list-note-field: down
BC-list-note-section: Planets
---

# Section List Note

**Builder:** `list_note` + `BC-list-note-section`

Same list-note builder, but `BC-list-note-section: Planets` scopes it to a **single heading**. Only the wiki-links under `## Planets` become `down` children. Lists in other sections (`## Appendix`) are ignored.

The section runs from its heading to the next heading of equal-or-higher level (or end of file), so nested sub-headings stay inside it.

## Planets

- [[Mercury]]
- [[Venus]]

## Appendix

- [[Pluto]]

> Pluto is in `## Appendix`, so it gets **no** edge. Only Mercury and Venus are children.
