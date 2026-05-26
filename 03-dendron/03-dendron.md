---
up: "[[Home]]"
---

# Dendron Note

**Builder:** `dendron_note`

Hierarchy inferred from dot-delimited basenames. No frontmatter required on child notes — the filename alone defines the tree.

**Setting:** `dendron_note.enabled: true` (already on in this vault's `data.json`).

## Structure demonstrated

```
03-dendron (manual up to Home)
product                     ← root
product.design              ← child of product
product.design.typography   ← grandchild
product.engineering         ← child of product (sibling of design)
product.engineering.api     ← grandchild
product.engineering.testing ← grandchild (sibling of api)
```

Open `product.design.typography` and check the Trail — it reads `product > product.design > product.design.typography`.
