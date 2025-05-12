# catppuccin-tty
A theme for the Linux vconsole.  Because yes.

This is a fork of [gh:lewisacidic/nord-tty](https://github.com/lewisacidic/nord-tty)


## Usage

When in a boring, normal Linux vconsole (e.g. by pressing `Ctrl`+`Alt`+`2`), source the file:

```sh
source catppuccin-[latte, frappe, macchiato, mocha]-tty
```

Cool hint: you can put this in your `.{bash,zsh}rc`, if you put multiple of them only the last one will work fyi.


## How does it work?

It sets the 16 console colors to those employed by nord with the appropriate ANSI escape sequences.
Specifically, these are `\e]PXRRGGBB` where X is the color index, and RRGGBB is a color expressed in hexadecimal format.
These can be printed using `echo` with the `-en` flags.


## Add to login screen
wip

If you just can't wait until you log in for the nord-ttyness, you can add the commands to the start of `/etc/issue` to run before the login prompt:

```sh
cat nord-tty.issue /etc/issue > /tmp/issue && sudo mv /tmp/issue /etc/issue
```

