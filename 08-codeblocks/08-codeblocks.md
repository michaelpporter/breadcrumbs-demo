---
up: "[[Home]]"
---

# Codeblocks

**Feature:** ` ```breadcrumbs ``` ` fenced blocks in notes

Render a hierarchy inline — useful for MOCs, indexes, and visualizations. Three renderers: `tree`, `mermaid`, `markmap`.

## Examples

See individual notes for live examples:

- [[Codeblock Tree]] — tree renderer, most common
- [[Codeblock Mermaid]] — Mermaid flowchart
- [[Codeblock Markmap]] — interactive mind map

## Codeblock schema

```
type: tree | mermaid | markmap
title: "optional heading"
start-note: "path/to/note"   # default: active note
field: up | down | same      # which field to traverse
depth: 3                     # max depth
flat: false                  # flat list vs nested
```
