---
up: "[[08-codeblocks]]"
---

# Codeblock Tree

Renders a nested tree from a given note's descendants.

## Example — tree from Project Alpha

````breadcrumbs
type: tree
start-note: "01-typed-link/Project Alpha.md"
fields: [down]
depth: [3]
title: "Project Alpha hierarchy"
````

## Example — flat list of children

````breadcrumbs
type: tree
start-note: "01-typed-link/Project Alpha.md"
fields: [down]
depth: [1]
flat: true
title: "Direct children of Project Alpha"
````
