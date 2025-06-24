# xbps

> A simple, user-friendly wrapper around Void Linux’s `xbps` package manager.

**xbps** makes installing, removing, searching, and managing packages on Void Linux faster and more intuitive, using concise syntax and optional dry-run support.

## Features

- Short aliases for common tasks (`+` for install, `-` for remove, `/` for search)
- Install/remove multiple packages at once
- Search and view detailed package info
- System upgrade support
- Dry-run mode to preview commands
- Auto-logs all installs/removals to `~/.xbps_wrapper.log`
- Colorized terminal output for better UX

## Usage

```bash
xbps [COMMAND] [PKGS...] [--dry-run]
```

| Command      | Alias | Description                           |
|--------------|-------|---------------------------------------|
| `install`    | `+`   | Install one or more packages          |
| `remove`     | `-`   | Remove one or more packages           |
| `search`     | `/`   | Search for packages by name           |
| `info`       | `i`   | Show detailed info for a package      |
| `upgrade`    | `u`   | Upgrade all installed packages        |
| `list`       | `ls`  | List all installed packages (paged)   |
| `version`    |       | Show current version                  |
| `help`       |       | Display usage guide                   |

### Optional Flags

| Flag        | Description                                   |
|-------------|-----------------------------------------------|
| `--dry-run` | Preview the commands without running them     |


## Examples

```bash
xbps + vim git curl           # Install multiple packages
xbps - nano                   # Remove nano
xbps / terminal               # Search for packages with "terminal" in name
xbps i ffmpeg                 # View info for ffmpeg
xbps u                        # System upgrade
xbps ls                       # List installed packages
xbps + htop --dry-run         # Simulate install (no action taken)
```

## Log File

All install, remove, and upgrade actions are logged to:

```
~/.xbps_wrapper.log
```

## Installation

Just clone and place the script somewhere in your `PATH`:

```bash
git clone https://github.com/KDesp73/xbps
cd xbps
chmod +x xbps
sudo mv xbps /usr/local/bin/
```

## License

MIT License.
See [`LICENSE`](./LICENSE) for details.

