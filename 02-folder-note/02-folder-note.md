---
up: "[[README|home]]"
BC-folder-note-field: down
BC-folder-note-recurse: true
---

# Folder Note

**Builder:** `folder_note`

Add `BC-folder-note-field: down` to any note and Breadcrumbs treats it as the index for its containing folder — creating `down` edges to every other file in the folder.

Set `BC-folder-note-recurse: true` to recurse into subfolders.

## Structure demonstrated

```
02-folder-note (this file = folder index)
└── Engineering/
    ├── Engineering (folder index)
    ├── Backend/
    │   ├── Backend (folder index)
    │   ├── API Design
    │   └── Database Schema
    └── Frontend/
        ├── Frontend (folder index)
        ├── Component Library
        └── Routing
```

Each folder has an index note with `BC-folder-note-field: down`. Breadcrumbs auto-links every file in that folder as a child.
