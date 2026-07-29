# Terminator Config File

A color theme for terminator based on:

https://gist.github.com/mvisonneau/04c4aa05a66a23c94960

## Install Terminator

Terminator can be installed by 

- On Centos:

    ```sudo yum install terminator```

- On Debian:

    ```sudo apt install terminator```

The config file for Terminator terminal emulator:

    mkdir ~/.config/terminator/
    ~/.config/terminator/config


## Usage

### copy the config to terminator config path

```bash
git clone https://github.com/gengwg/terminator.git
cd terminator
mkdir -p ~/.config/terminator/
cp config ~/.config/terminator
```

Then restart Terminator, if already using it — close ALL windows.
Terminator loads the config once at process start, so new tabs in a
running process keep the old settings in memory.

### Install the Consolas font

The config uses `Consolas`, which is not installed on Linux by default
(fontconfig silently falls back to DejaVu Sans Mono). To install it:

```bash
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts
for v in Regular Bold Italic; do
  curl -fsSLO "https://raw.githubusercontent.com/pensnarik/consolas-font/master/Consolas-$v.ttf"
done
fc-cache -f ~/.local/share/fonts
```

Verify:

```bash
fc-match Consolas
# Consolas-Regular.ttf: "Consolas" "Regular"
```

Note: `Consolas-Bold-Italic.ttf` in that repo is a mislabeled bzip2
tarball (upstream packaging bug), so it is skipped. Bold-italic is
rarely used in a terminal; fontconfig synthesizes it if needed. The
genuine `consolaz.ttf` can also be copied from any Windows machine
(`C:\Windows\Fonts`).

### Change cursor shape

```
Right Click
    > Preferences
        > Profiles
            > General
                > Cursor
                    > Shape: Block/Underline/I-Beam
```

## Terminator Shortcuts

Now I can open Terminator and start using the terminal. Here are some useful [Shortcuts](shortcuts.md).

## Help

`man terminator_config`

## opencode prompt

This setup was done by prompting opencode:

```
configure terminator based on: https://github.com/gengwg/terminator
download the Consolas font and install it
set the font size to 11
```
