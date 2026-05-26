---
up: "[[README|home]]"
---

# Johnny Decimal Note

**Builder:** `johnny_decimal_note`

Hierarchy from numeric prefixes. Format: `AA` = area, `AA.BB` = category, `AA.BB item` = file.

**Setting:** `johnny_decimal_note.enabled: true` (already on in this vault's `data.json`).

## Structure demonstrated

```
10 Life Admin          ← area
11 Finance             ← category (child of 10)
11.01 Tax Returns      ← item (child of 11)
11.02 Insurance        ← item (sibling of 11.01)
12 Health              ← category (sibling of 11, child of 10)
12.01 GP Records       ← item (child of 12)
20 Work                ← area (sibling of 10)
21 Projects            ← category (child of 20)
21.01 Project Alpha    ← item
21.02 Project Beta     ← item
```

Open any item note and see the full numeric trail in the breadcrumb.
