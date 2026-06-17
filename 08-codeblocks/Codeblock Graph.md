---
up: "[[08-codeblocks]]"
---

# Codeblock Graph

Renders the **whole graph** as a Mermaid diagram, instead of traversing out from a
single note. Use `from:` to scope it to a subset of notes (`#tag`, `"folder"`,
`[[link]]`, combined with `AND` / `OR` / `NOT`).

## Example — the whole vault (filtered to one field)

````breadcrumbs
type: graph
fields: [up]
title: "Every up-edge in the vault"
````

## Example — a folder as a subgraph

````breadcrumbs
type: graph
from: '"03-dendron"'
fields: [down]
depth: [3]
title: "Dendron subgraph"
````
