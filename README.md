# twitchmpv
Wrapper bash script for streamlink in order to more simply watch twitch from the terminal.

## Installation
### Dependencies
- [streamlink](https://github.com/streamlink/streamlink)
- [mpv](https://github.com/mpv-player/mpv)

### Manual Installation
1. Clone the repository
2. Copy the `twitchmpv` script to a directory in your `$PATH` for example into `$HOME/.local/bin`
3. Make the script executable with `chmod +x twitchmpv`

### Arch Linux
There is an AUR package available: [twitchmpv-git](https://aur.archlinux.org/packages/twitchmpv-git/)
```bash
yay -S twitchmpv-git
```

## Usage
```bash
twitchmpv <channel or url> [quality] ["streamlink options"]
```

### Config file
You can create a config file at `$HOME/.config/twitchmpv/config` to set your twitch oauth token and client id.
```
# Example config file
twitchOauth = abcdefghijklmnopqrstuvwxyz
twitchClientId = abcdefghijklmnopqrstuvwxyz
defaultQuality = best
```

