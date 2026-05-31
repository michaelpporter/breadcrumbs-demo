---
up: "[[HOME|home]]"
---

# Traverse Note

**Builder:** `traverse_note`

A note annotated with `BC-traverse-note-field: <field>` becomes a traversal root. Breadcrumbs performs a depth-first search (DFS) through the Obsidian vault link graph starting from that note — following regular wiki-links, not BC fields — and creates one edge per parent→child hop, all typed with the specified field.

No special frontmatter is needed on the linked notes. The hierarchy is inferred entirely from ordinary `[[wikilinks]]`.

**Frontmatter key:** `BC-traverse-note-field: down`

## Structure demonstrated

```
Knowledge Map          ← BC-traverse-note-field: down
├── Programming        ← linked from Knowledge Map
│   ├── Python         ← linked from Programming
│   └── JavaScript     ← linked from Programming
└── History            ← linked from Knowledge Map
    ├── Ancient Rome   ← linked from History
    └── Renaissance    ← linked from History
```

Open **Knowledge Map** and check the **Tree View** — the full hierarchy appears even though only `Knowledge Map` has a BC frontmatter field.
