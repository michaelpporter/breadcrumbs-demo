---
up: "[[Home]]"
---

# Date Note

**Builder:** `date_note`

Breadcrumbs auto-links daily notes by date. Files named `yyyy-MM-dd` get `next`/`prev` edges to adjacent dates — no frontmatter needed.

**Settings in `data.json`:**
- `date_note.enabled: true`
- `date_format: "yyyy-MM-dd"`
- `default_field: "next"`

## Structure demonstrated

Seven consecutive days. Open any day note and use Prev/Next navigation to walk the chain.

```
2024-03-01 → 2024-03-02 → 2024-03-03 → 2024-03-04 → 2024-03-05 → 2024-03-06 → 2024-03-07
```

> Note: `stretch_to_existing: false` means Breadcrumbs only links dates that have files. If you delete `2024-03-04`, the chain breaks at that point. Set it to `true` to bridge gaps.
