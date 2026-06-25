# Mono MD

A minimal local text editor with Markdown preview.

## Philosophy

Mono MD is intentionally small.

* Zero dependencies
* Single HTML file (`index.html`)
* No build step
* No npm
* No backend
* No configuration
* Local files only

Markdown preview is the only special feature.

Everything else is just plain text.

## Features

* `Cmd + O` : Open local file
* `Cmd + Shift + O` : Reopen a recent file
* `Cmd + S` : Save file
* `Cmd + /` : Toggle Markdown preview (`.md` only)

Unsaved edits are marked with a `●` in the footer. An untitled buffer is saved
as a local draft and restored when you reopen the editor, so a quick note is
never lost — and closing it shows no prompt. For a file with unsaved edits,
closing the tab or window triggers the browser's confirmation prompt.

## File Types

| Extension | Behavior        |
| --------- | --------------- |
| `.md`     | Edit + Preview  |
| Others    | Plain text edit |

## Non-goals

Mono MD intentionally does **not** provide:

* Syntax highlighting
* LSP
* Auto completion
* Project management
* Plugins
* Themes
* Cloud sync
* AI integration
* Package manager

If you need those features, use another editor.

Mono MD aims to be a quiet place for writing and editing local files.
