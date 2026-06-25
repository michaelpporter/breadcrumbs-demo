---
up: "[[HOME|home]]"
BC-list-note-field: down
BC-list-note-neighbour-field: next
BC-list-note-section: Children
---

# List Note

**Builder:** `list_note`

This note is the list-note index. Breadcrumbs reads the wiki-links in the list below and creates `down` edges to each linked note. With `BC-list-note-neighbour-field: next`, consecutive items also get `next`/`prev` edges.

**Setting:** `list_note.default_neighbour_field: "next"` in `data.json` (can override per-note with `BC-list-note-neighbour-field`).

## Children

- [[Apple]]
	- [[Apple Pie]]
	- [[Apple Juice]]
- [[Banana]]
- [[Cherry]]
- [[Durian]]
- [[Elderberry]]

> **Order matters** — items at the *same indent* chain by `next`/`prev`:
> `Apple → Banana → Cherry → Durian → Elderberry`.

**Nesting re-parents.** Only top-level bullets become children of *this* note; a nested bullet is a child of the bullet above it, and keeps its own `next`/`prev` chain at its own indent level:

- `Apple → down → Apple Pie` and `Apple → down → Apple Juice` (children of **Apple**, not the index)
- `Apple Pie → next → Apple Juice` (a separate sub-chain — it does **not** continue to Banana)

## See also

Documentation links, not children — this note sets `BC-list-note-section: Children`, so the builder only reads the list under `## Children` above. Without it, these two would be pulled in as `down` children and spliced into the `next`/`prev` chain.

- [[Section List Note]] — scope the builder to one heading with `BC-list-note-section`.
- [[Exclude List Note]] — exempt individual links with `BC-list-note-exclude`.
