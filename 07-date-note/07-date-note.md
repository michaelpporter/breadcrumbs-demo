---
up: "[[HOME|home]]"
---

# Date Note

**Builder:** `date_note`

Breadcrumbs auto-links date notes by parsing filenames — no frontmatter needed. Period notes form a containment hierarchy: daily → weekly → monthly → quarterly → yearly.

**Settings in `data.json`:**
- `date_note.enabled: true`
- `date_format: "yyyy-MM-dd"` (daily)
- `default_field: "next"`
- Weekly: `next_field: "next_week"`, `up_field: "up"`, format `kkkk-'W'WW`
- Monthly: `next_field: "next_month"`, `up_field: "up"`, format `yyyy-MM`
- Quarterly: `next_field: "next_quarter"`, `up_field: "up"`, format `yyyy-'Q'q`
- Yearly: `next_field: "next_year"`, `up_field: "up"`, format `yyyy`

## Structure

```
07-date-note/
  2024.md / 2025.md / 2026.md    ← yearly notes
  2024/
    DAILY/03/      ← 7 consecutive days (basic next/prev chain)
    MONTHLY/       ← 2024-03
    QUARTERLY/     ← 2024-Q1
    WEEKLY/        ← 2024-W09, 2024-W10
  2025/
    MONTHLY/       ← full year (12 months)
    QUARTERLY/     ← Q1–Q4
  2026/
    DAILY/05/      ← workdays May (weekends skipped)
    DAILY/06/      ← early June
    MONTHLY/       ← 2026-01 through 2026-06
    QUARTERLY/     ← 2026-Q1, 2026-Q2
    WEEKLY/        ← 2026-W18 through 2026-W23
```

## What to explore

- Open any daily note → Prev/Next walks the date chain
- Daily note → `up` → week note → `up` → month → `up` → quarter → `up` → year
- Transitive rules (rounds: 3) chain `up` across levels automatically
- May 2026 weekends are missing — toggle `stretch_to_existing` to bridge gaps
