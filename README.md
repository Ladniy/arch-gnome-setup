# Arch & Gnome Ladniy's Set-up

Hi there! There is a repo with overview and a bunch of instructions for my own Arch & Gnome system.

For now it is pretty raw, but I hope it will get better in the future!

# Make apps looks consistently:

## Adwaita GTK3 Theme (Gnome Theme)
* Install [adw-gtk-3 (AUR)](https://aur.archlinux.org/packages/adw-gtk3) and [gnome-tweaks](https://archlinux.org/packages/extra/any/gnome-tweaks/)
* Set adw-gtk-3 theme for legacy apps in Gnome Tweaks

## Rounded Window Corners (Gnome Extension)

* Install extension from [here](https://extensions.gnome.org/extension/5237/rounded-window-corners/) (if it's actually updated, for current moment update for Gnome 45 still not pushed in mainstream)
* If extension still not officially updated, then download this [archive (github.com)](https://github.com/in4matix/Gnome45-Extensions) and install it manually
  * Put 'rounded-window-corners@yilozt' folder in this directory `/home/example/.local/share/gnome-shell/extensions/`
  * Relog into session

# Extensions:

## Currently used and recommended by me:
* Rounded Window Corners
* gTile

## I would like to try:
* [Color Picker](https://extensions.gnome.org/extension/3396/color-picker/)
* [Forge](https://extensions.gnome.org/extension/4481/forge/)
* [Pano](https://extensions.gnome.org/extension/5278/pano/)
* [Blur My Shell](https://extensions.gnome.org/extension/3193/blur-my-shell/)
* [Just perfection](https://extensions.gnome.org/extension/3843/just-perfection/)

# Printer setup:

Currently I use HP LaserJet P1102S and it's doesn't work with clear cups, so it's need some additional steps

* Install [cups](https://archlinux.org/packages/extra/x86_64/cups/) and [system-config-printer](https://archlinux.org/packages/extra/x86_64/system-config-printer/)
  * `sudo pacman -S cups system-config-printer`
* Enable & start `cups.service`
  * `systemctl enable cups.service`
  * `systemctl start cups.service`
* Install [hplip-plugin (AUR)](https://aur.archlinux.org/packages/hplip-plugin)
  * `paru -S hplip-plugin`
* Go into Settings -> Printers and add printer
* Manually set driver to `HP LaserJet Professional p1102`
