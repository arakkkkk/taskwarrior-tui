# Taskwarrior TUI

[![CI](https://github.com/kdheepak/taskwarrior-tui/workflows/CI/badge.svg)](https://github.com/kdheepak/taskwarrior-tui/actions?query=workflow%3ACI)
[![](https://img.shields.io/github/license/kdheepak/taskwarrior-tui)](./LICENSE)
[![](https://img.shields.io/github/v/release/kdheepak/taskwarrior-tui)](https://github.com/kdheepak/taskwarrior-tui/releases/latest)
[![](https://img.shields.io/static/v1?label=platform&message=linux-32%20%7C%20linux-64%20%7C%20osx-64%20%7C%20win-32%20%7C%20win-64&color=lightgrey)](https://github.com/kdheepak/taskwarrior-tui/releases/latest)

A Terminal User Interface for [Taskwarrior](https://taskwarrior.org/).

![taskwarrior-tui](https://user-images.githubusercontent.com/1813121/89620056-4ed64200-d84c-11ea-9153-9e08bc26d3b4.gif)

## Installation

You will need to install `taskwarrior` first. See <https://taskwarrior.org/download/> for more information.

**Manual**

1. Download the tar.gz file for your OS from [the latest release](https://github.com/kdheepak/taskwarrior-tui/releases/latest).
2. Unzip the tar.gz file
3. Run with `./taskwarrior-tui`.

**Using [`zdharma/zinit`](https://github.com/zdharma/zinit)**

Add the following to your `~/.zshrc`:

```zsh
zinit ice wait:2 lucid extract"" from"gh-r" as"command" mv"taskwarrior-tui* -> tt"
zinit load kdheepak/taskwarrior-tui
```

**Using `cargo`**

```
git clone https://github.com/kdheepak/taskwarrior-tui.git
cd taskwarrior-tui
cargo build --release
```

**Using `AUR`**

Use your favorite installation method to download the [AUR package](https://aur.archlinux.org/packages/taskwarrior-tui-git/) maintained by [**@loki7990**](https://github.com/loki7990).

## Usage

- `/`: `task {string}`                       - Filter task report
- `a`: `task add {string}`                   - Add new task
- `d`: `task {selected} done`                - Mark task as done
- `e`: `task {selected} edit`                - Open selected task in editor
- `j`: `{selected+=1}`                       - Move down in task report
- `k`: `{selected-=1}`                       - Move up in task report
- `l`: `task log {string}`                   - Log new task
- `m`: `task {selected} modify {string}`     - Modify selected task
- `q`: `exit`                                - Quit
- `s`: `task {selected} start/stop`          - Toggle start and stop
- `u`: `task undo`                           - Undo
- `x`: `task delete {selected}`              - Delete
- `A`: `task {selected} annotate {string}`   - Annotate current task
- `?`: `help`                                - Help menu
- `!`: `{string}`                            - Custom shell command

![taskwarrior-tui](https://user-images.githubusercontent.com/1813121/88654924-40896880-d08b-11ea-8709-b29cc970da4c.gif)

`taskwarrior-tui` supports readline-like navigation:

- `<Ctrl-a>` : Go to beginning of the line
- `<Ctrl-e>` : Go to end of the line
- `<Ctrl-u>` : Delete from beginning of the line
- `<Ctrl-k>` : Delete to end of the line
- `<Ctrl-w>` : Delete previous word

![taskwarrior-tui](https://user-images.githubusercontent.com/1813121/95651612-ce7cc900-0aa8-11eb-8686-42442ed9ee43.gif)
