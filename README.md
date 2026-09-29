# Herdr Cheatsheet

> **English** · [한국어](README.ko.md)

A single-file, print-friendly cheatsheet of the most-used [Herdr](https://herdr.dev/docs/) keybindings and CLI commands: pane splits, tabs, workspaces, sessions, agents, plus a copy-paste **agent setup prompt** that installs Herdr globally and pulls the official [SKILL.md](https://github.com/herdrdev/herdr/blob/master/skills/herdr/SKILL.md).

Open `index.html` directly, or visit the GitHub Pages site → https://cskwork.github.io/herdr-cheatsheet/

## What's inside

- **Install** block: one-liners for curl / brew / mise / Windows.
- **Agent setup prompt**: one prompt to install Herdr globally and teach your coding agent the CLI.
- **Prefix keybindings**: panes (vertical/horizontal split, close, zoom, resize, swap), tabs (new, next/prev, switch 1-9, rename, close), workspaces (picker, new, rename, close, worktree), session (detach, sidebar, copy mode, help).
- **CLI essentials**: launch, server, sessions, workspaces, tabs, panes, agents, wait, update.
- **Agent states**: blocked / working / done / idle / unknown.

## Features

- Click any keycap or command to copy.
- Live search across every command.
- Print stylesheet (two-column, no chrome).
- Single self-contained `index.html` (no build step). Geist + JetBrains Mono via Google Fonts.
- Korean/English toggle (top-right KO/EN). Auto-detects the browser language on first visit; the choice is saved to `localStorage`.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## GitHub Pages

The repo is set up for GitHub Pages from the root of `main` (`.nojekyll` included). Enable Pages in repo Settings, or via `gh`:

```sh
gh repo create herdr-cheatsheet --public --source=. --push
gh api -X POST /repos/<user>/herdr-cheatsheet/pages -f "build_type=workflow" \
  -f "source[branch]=main" -f "source[path]=/"
```

Not affiliated with Herdr. Built from the official docs.
