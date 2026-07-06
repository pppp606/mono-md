# Mono MD

A minimal local text editor with Markdown preview.

**[Try it in your browser](https://pppp606.github.io/mono-md/)** — nothing to
install. The demo is `index.html` from `main`, served as-is: no build, no
bundling, exactly the file in this repository. Requires Chrome or Edge (the
editor uses the File System Access API).

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
* `Cmd + Shift + O` : Switch to a recent file or an unsaved draft
* `Cmd + S` : Save file
* `Cmd + /` : Toggle Markdown preview (`.md` only)

Unsaved edits are marked with a `●` in the footer, and closing the tab or
window while there are unsaved changes triggers the browser's confirmation
prompt.

### Drafts

Unsaved buffers are autosaved as drafts in the browser (IndexedDB) so an
accidentally closed tab is recoverable. `Cmd + Shift + O` lists drafts next to
recent files, newest first, each titled by its first line. Opening anything
from the picker preserves the document you were on, so it doubles as a way to
switch between notes in a single tab. A draft is dropped once it is saved to a
real file (`Cmd + S`) or emptied. Drafts never leave your machine.

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
