# final (i hope) chad setup

## detailed log to transform into a guide later

## prerequisites

a sha checked download of the latest arch iso flashed onto a usb stick

## install

straight up archinstall, mostly with default settings. noteworthy:

- it keyboard layout
- german mirrors
- best effort ext4 partitioning
- tp/dvh => host/username
- sway profile with polkit
- intel open drivers
- ly greeter
- pipewire and bluetooth
- rome timezone

## first boot

cool thing is all the basis are covered with this installer. first things i did:

- install firefox, fastfetch, micro (set catppuccin for micro instant :) )
- minimal sway setup to make it usable
- installed paru and typora from the aur (paru seems the most modern aur helper)
- installed nwg-look to get dark mode asap
- install iosevka term nerd
- install wezterm
- install tlp!

## mvp wezterm tangent

no point specifying everything, i'll upload the wez lua config (yeah lua :) ) when i'm done.

- set it in sway for now

## shellz

- install fish (upload config file)
- setup micro (upload config file)
- install starship (upload config file)
- install: lsd, nerdfetch, bat, btop (for btop disable background color in conf)
- install and setup yazi file manager
- set catppuccin mocha (green if accented) for literally everything (not included in all dotfiles so specifying)

## editorz

- install helix
- set catppuccin mocha with the transparency trick

## finally back to sway for a bit

- install the catppuccin cursors (green obv)
- download the awesome green catppuccin mandelbrot bg
- install the inter font and ibm plex serif as i'm at it (for firefox later)
- the full dotfile will be specified
- install gammastep to make night mode work
- install workstyle for chad workspace names

## give sway a fine status bar

- i think i'll settle with i3status-rust
- ok just finished configuring an mvp, seems cool :)

## notifications

- setup mako

## browser (firefox)

- with gtk customization and fonts setup we can completely setup the browser finally
- setup settings as usual (keep tabs, clean start screen, play drm...), setup inter as sans font, iosevka as the monospace, leave dejavu as serif
- cleanup tab bar, keep only dark reader and stylus extensions pinned
- install extensions: ublock origin, dark reader, youtube dislike and sponsorblock
- install firefox catppuccin mocha green theme
- set dark reader catppuccin theme
- install catppuccin web icons
- install catppuccin user styles customized for visited websites and green accent
- remove x button using userchrome

## app launching

- tofi, config file to upload

## setup ly config (to upload)

## cleanup boot screen

- set systemd-boot timeout to 0
- add kernel params speficied in arch wiki

## cleanup the sway default profile extra

- waybar
- foot
- wmenu