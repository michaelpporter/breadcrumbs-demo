---
up: "[[Home]]"
down:
  - "[[Project Alpha]]"
  - "[[Project Beta]]"
---

# Typed Link

**Builder:** `typed_link`

Explicit edges via frontmatter. Add `up`, `down`, `same`, `next`, or `prev` fields to any note. Values are wiki-links (single or list).

Implied relations automatically create the reverse edge — e.g. `up` on this note → Breadcrumbs adds a `down` edge from `Home` back here.

## Structure demonstrated

```
Home
└── 01-typed-link          ← down: Project Alpha, Project Beta
    ├── Project Alpha      ← down: Task One, Task Two
    │   ├── Task One       ← same: Task Two, next: Task Two
    │   │   ├── Subtask A
    │   │   └── Subtask B
    │   └── Task Two       ← same: Task One, prev: Task One
    └── Project Beta
        └── Milestone 1
```
