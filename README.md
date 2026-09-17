# tmux-taskbar

A single-file Bash tmux taskbar with optional status extensions.

## Install

Clone this repository and run:

```bash
./user-tmux-taskbar --install
```

The installer links the generated tmux configuration into `~/.tmux.conf`,
adds the taskbar command to `PATH`, and preserves existing configuration in
timestamped backup files. Run `./user-tmux-taskbar --start` to start a new
taskbar session, or `./user-tmux-taskbar --settings` to configure it.

## Included extensions

The extensions live in `user-tmux-taskbar-data/` and report Codex quota,
geopolitical risk, network rates and totals, operating-system updates,
temperature, and uptime. They are discovered automatically when the taskbar
runs.

Generated configuration, cache, state, logs, and backups are intentionally
ignored by Git; personal settings remain local to the installation.

## Requirements

- Bash
- tmux
- Linux for the system/network/thermal extensions
- `curl` and `python3` for the geopolitical-risk extension
