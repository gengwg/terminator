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

Then restart Terminator, if already using it.

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

Now I can open Terminator and start using the terminal. Here are some useful [Shortcuts](terminator.md).

## Help

`man terminator_config`
