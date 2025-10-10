# dvh's chad thinkpad configuration

> october 2025 edition

this will be a step by step description of how i setup my thinkpad linux configuration.

## philosophy

- **minimalism**: small, lightweight, to the point, as few moving parts as possible
- **ease of configuration**: no infinite configuration settings to waste time on (i like simple config files, no css or weird stuff)
- **modern**: maintained, future-aware choices
- **stable**: no experimental stuff, less points of failure
- **beautiful and fun**: heck, i need to use the system everyday, it might as well be pleasant

## core components

- **base distro**: [glibc void](https://voidlinux.org/) (rolling release but more stable, no systemd, small and maintained, glibc still safer)
- **window manager**: [sway](https://swaywm.org/) (de-facto wayland window manager, stable) *and all the tools that come with it
- **terminal emulator**: [foot](https://codeberg.org/dnkl/foot) (wayland-first and minimal)
- **code editor**: [helix](https://helix-editor.com/) (terminal-based with more features than micro and not as overwhelming as neovim)
- **web browser**: [firefox](https://www.firefox.com/) (de-facto linux web browser, not much choice to be fair) *remember to launch in wl mode
- **font**: [iosevka](https://www.nerdfonts.com/) (beautiful font, perfect for small screen because it's compact)
- **shell**: [fish](https://fishshell.com/) (great defaults, nice to use)
- **md editor**: [typora](https://typora.io/) (not open, but just too good) *doesn't have a catppuccin port, but i could work on that :)
- **notification daemon**: [mako](https://github.com/emersion/mako) (seems the best)
- **menu**: [tofi](https://github.com/philj56/tofi) (seems the tiniest and fastest)
- **theme**: [catppuccin mocha](https://catppuccin.com/) (i love it, also it has ports for all of the above and more!)
- **misc**: tlp, fastfetch, btop, lsd, bat

## setup

- download the latest **x86_64 base glibc live image** for void [here](https://repo-default.voidlinux.org/live/current/)
- flash to a usb stick using [balena etcher](https://etcher.balena.io/) or the **dd** command
- boot and follow the [installation instructions](https://docs.voidlinux.org/installation/live-images/guide.html)

-> for help with the partitioning i followed [this guide](https://www.youtube.com/watch?v=IBg66Us2f6g)

## first boot

nice! we're in. first thing to run is a nice:

```bash
sudo xbps-install -Su
```

it will probably ask to update the package manager, just follow the instructions.

then, priorities first:

```bash
sudo xbps-install fastfetch
fastfetch
```

ahh, perfect.

- update [firmware](https://docs.voidlinux.org/config/firmware.html)
- setup [cron](https://docs.voidlinux.org/config/cron.html) and [ssd](https://docs.voidlinux.org/config/ssd.html)
- disable acpid service, setup elogind and tlp, explained all [here](https://docs.voidlinux.org/config/power-management.html)
- setup [dbus](https://docs.voidlinux.org/config/session-management.html)
- install all [graphics drivers](https://docs.voidlinux.org/config/graphical-session/graphics-drivers/index.html)

nearly there:

```bash
sudo xbps-install nerd-fonts
sudo xbps-install foot
sudo xbps-install sway
```

finally, running this command we should get into the graphical environment and be able to launch terminals using super + enter:

```bash
dbus-run-session sway
```

cool, now we have a good functional base, to aid in this process i have installed some extra packages at this point:

```bash
sudo xbps-install micro
```
