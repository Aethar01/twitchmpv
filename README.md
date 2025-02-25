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
```
   Usage: twitchmpv -n|--name <channel name or url> [options] -- [streamlink arguments]

   Watch Twitch streams with mpv using streamlink.

   Options:
   -h, --help              Show this help message and exit
   -c, --config            Set the path to the config file
   -q, --quality           Set the quality of the stream
   -n, --name              Set the name of the twitch channel, can also be a twitch url. Required.
   -a, --audio-only        Disable video playback
   -d, --disown            Disown the process (if you run with -a and -d, you can only kill the process manually)
   -s, --silent            Run streamlink in silent mode
   -v, --verbose           Print debug information
   -l, --low-latency       Enable low latency mode
   --                      Pass additional arguments to streamlink
```

### Config file
You can create a config file at `$HOME/.config/twitchmpv/config` to set your twitch oauth token and client id.
```
# Example config file
twitchOauth = abcdefghijklmnopqrstuvwxyz
twitchClientId = abcdefghijklmnopqrstuvwxyz
defaultQuality = best
disown = (0|1)
silent = (0|1)
noVideo = (0|1)
lowLatency = (0|1)
```

