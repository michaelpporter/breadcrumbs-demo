---
up: "[[README|home]]"
BC-list-note-field: down
BC-list-note-neighbour-field: next
---

# List Note

**Builder:** `list_note`

This note is the list-note index. Breadcrumbs reads the wiki-links in the list below and creates `down` edges to each linked note. With `BC-list-note-neighbour-field: next`, consecutive items also get `next`/`prev` edges.

**Setting:** `list_note.default_neighbour_field: "next"` in `data.json` (can override per-note with `BC-list-note-neighbour-field`).

## Children

- [[Apple]]
- [[Banana]]
- [[Cherry]]
- [[Durian]]
- [[Elderberry]]

> The order matters! Apple → next → Banana → next → Cherry, etc.
