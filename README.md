# breadcrumbs-demo

An Obsidian vault demonstrating every edge-builder in the [Breadcrumbs plugin](https://github.com/michaelpporter/breadcrumbs). Each folder is a self-contained example you can open, inspect, and extend.

## What is Breadcrumbs?

Breadcrumbs adds structured navigation to Obsidian by letting you define directional relationships between notes — `up`, `down`, `same`, `next`, `prev` — using a variety of automatic and manual methods called **edge-builders**. Once edges are defined, the plugin renders trails, trees, and matrices so you can navigate your vault hierarchically.

## Demos

| Folder | Edge-builder | Technique |
|---|---|---|
| `01-typed-link` | `typed_link` | Manual frontmatter fields (`up`, `down`, `same`, `next`, `prev`) |
| `02-folder-note` | `folder_note` | Folder structure inferred via `BC-folder-note-field` |
| `03-dendron` | `dendron_note` | Dot-delimited basenames (`project.frontend.components`) |
| `04-johnny-decimal` | `johnny_decimal_note` | Numeric prefix hierarchy (`11.01 Invoice`) |
| `05-list-note` | `list_note` | Markdown list items become child notes |
| `06-tag-note` | `tag_note` | Tag hub notes link all tagged notes as children |
| `07-date-note` | `date_note` | Daily notes auto-linked by `next`/`prev` |
| `08-codeblocks` | — | `breadcrumbs` codeblock render types (tree, trail, markmap) |
| `09-traverse-note` | `traverse_note` | DFS walk of vault links from a root note |

## Getting started

> **Requires Obsidian 1.13.0 or newer.**

1. Clone or download this repo.
2. Open the root folder as a vault in Obsidian (**Open folder as vault**).
3. Enable the **Breadcrumbs** community plugin (Settings → Community plugins).
4. Plugin settings are pre-configured via `.obsidian/plugins/breadcrumbs/data.json` — no manual setup needed.
5. Open any folder's index note and explore the Trail, Tree View, and Matrix View.

## Resources

- [Breadcrumbs plugin repo](https://github.com/michaelpporter/breadcrumbs)
- [Breadcrumbs documentation](https://breadcrumbs-docs.michaelpporter.com)
