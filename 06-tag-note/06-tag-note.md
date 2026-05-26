---
up: "[[Home]]"
---

# Tag Note

**Builder:** `tag_note`

A "tag hub" note lists a tag in `BC-tag-note-tag`. Breadcrumbs finds every note in the vault with that tag and creates edges from the hub to each tagged note.

**Settings:** `tag_note.default_field: "up"` and `default_sibling_field: "same"` in `data.json`.

## Structure demonstrated

Three hubs, each collecting notes by tag:

| Hub | Tag | Notes |
|---|---|---|
| `Fruits Hub` | `#fruits` | Apple, Banana, Cherry |
| `Colors Hub` | `#color` | Red, Blue, Green |
| `Animals Hub` | `#animal` | Cat, Dog, Bird |

Open any hub and check the **Tree View** — it lists all tagged notes as children.
Open any tagged note (e.g. `Apple`) — the Matrix shows `Fruits Hub` as parent.
