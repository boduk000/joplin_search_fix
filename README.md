# Literal Search — Joplin Plugin

A search panel for Joplin that finds an **exact substring** across all your notes.
Every character in your query is taken **literally** (`-`, `*`, `|`, `$`, `.`, etc.) —
no full-text-search operators get in the way. Works with any language, including
matches **inside code blocks**.

Built because Joplin's built-in search treats `-word` as "exclude", `*` as a
wildcard and tokenizes punctuation — so technical strings like
`GetUserSPNs.py -request *` or `scp file user@host:~/` were impossible to find.

## Features
- **Literal substring search** — your query is matched verbatim, no operators.
- **Match case** and **Regex** toggles.
- Results show the **notebook path** (e.g. `HTB / Metasploit`), note title and the matching line.
- Click a result to **open the note and jump to the match**:
  - **Markdown editor:** scrolls to the match and **flash-highlights** it.
  - **Rich Text editor:** scrolls near the match (highlighting in the Rich Text
    editor is not possible — Joplin exposes no editor API for it).
- Keyboard shortcut: **Ctrl/Cmd + Shift + F** toggles the panel.

## Install
1. Download `literal-search.jpl` from the releases.
2. Joplin → **Tools → Options → Plugins**.
3. Click the gear next to *Manage your plugins* → **Install from file** → select the `.jpl`.
4. Restart Joplin.

## Usage
- Open the panel with the search button in the note toolbar or **Ctrl/Cmd+Shift+F**.
- Type your query exactly as it appears in your notes.
- Click any result to jump to it.

## Build from source
The plugin is plain JS (no bundler needed). To repackage:
