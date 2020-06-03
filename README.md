# My build of **suckless's dwm**

This build includes some patches (source is inside **'patches'** folder) and
personal configurations in **'config.h'** file.  
The **'colors-dwm.h'** file has my theme configuration for **dwm**.

## Original README

Bellow are the contents of the original README file from **suckless** with some
minor edits.

### dwm - dynamic window manager

dwm is an extremely fast, small, and dynamic window manager for X.

### Requirements

In order to build dwm you need the Xlib header files.

### Installation

Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

`make clean install`

### Running dwm

Add the following line to your _.xinitrc_ file to start dwm using `startx`:

`exec dwm`

In order to connect dwm to a specific display, make sure that
the **DISPLAY** environment variable is set correctly, e.g.:

`DISPLAY=foo.bar:1 exec dwm`

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your _.xinitrc_ file:

```sh
while xsetroot -name "`date` `uptime | sed 's/.*,//'`"; do
  sleep 1
done &
exec dwm
```

### Configuration

The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

## Patches credits

- [statuscmd patches](https://dwm.suckless.org/patches/statuscmd/):
  - Daniel Bylinka - daniel.bylinka@gmail.com
- [alpha patch](https://dwm.suckless.org/patches/alpha/):
  - Eon S. Jeon - esjeon@hyunmu.am
  - Laslo Hunhold - dev@frign.de (6.1 port)
  - Thomas Oltmann - thomas.oltmann.hhg@gmail.com (20180613-b69c870 port)
  - Jakub Leszczak - szatan@gecc.xyz (fixborders patch)
- [attachaside patch](https://dwm.suckless.org/patches/attachaside/):
  - Jerome Andrieux - jerome@gcu.info
  - Chris Down - chris@chrisdown.name (6.1 port and fixes)
  - Laslo Hunhold - dev@frign.de (git port)
- [cyclelayouts patch](https://dwm.suckless.org/patches/cyclelayouts/):
  cd
- [fakefullscreen patch](https://dwm.suckless.org/patches/fakefullscreen/)
  - Jan Hendrik Farr - farrjanhendrik@aol.de
- [fancybar patch](https://dwm.suckless.org/patches/fancybar/)
  - Mate Nagy - mnagy@port70.net
  - Jochen Sprickerhof (rewrite)
- [movestack patch](https://dwm.suckless.org/patches/movestack/)
  - Niki Yoshiuchi - <aplusbi@gmail.com>
  - Moritz Wilhelmy (fix to work with dwm 5.8) - <moritz plus suckless at wzff dot de>
- [ru gaps patches](https://dwm.suckless.org/patches/ru_gaps/)
  - Aaron Duxler - aaron@duxler.xyz
  - Rob Livesey - rlives6789@gmail.com
- [statuspadding patch](https://dwm.suckless.org/patches/statuspadding/)
  - cd
