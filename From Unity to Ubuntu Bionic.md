# Notes moving from Unity to Ubunto Bionic 

## Summary

- Update from 16.04 worked flawlessly.
- Unity is dead and does not work for me on 18.04.
- Budgie is nice, give it a try.
- Gnome 3 takes lots of memory.
- Wayland is unusable (slow, terrible touchpad driver, no screen sharing).
- Pop theme works great (used it in 16.04, using it now on 18.04 as 
  Pop-dark-slim).
- Fira fonts still awesome

## Must haves

I am now using Gnome3 on X11 with some extensions and the Pop theme and icons.
Before i used gnome-terminal with tmux but because of the removed overlay 
scroll bar support (also an issue with the lates 16.04 update), i am currently
trying tilix without tmux.

- Use X11, Wayland is still too limited
- Install gnome-tweak-tool to set themes and other stuff

## Wayland

I use screen sharing, not possible as of now with Wayland, thus X11 it is.
Also the T440p touchpad does work terrible with the Wayland touchpad driver
while it works perfectly with the X11 one.

To get rid of unusable Wayland even on the login screen, configuration in 
`/etc/gdm3/custom.conf` makes just that possible.

```
[daemon]
WaylandEnable=false
```

### Tweak tool extensions

- Places status indicator
- Removable drive menu
- Tilix dropdown
- Ubuntu appindicators - i use apps which use tray icons as app indicators
- Ubuntu dock
- Workspace indicator - i use workspaces to group stuff and keep it running
- Workspaces to dock - helps a bit with the vertical only workspaces and
  changes the way how to work with workspaces to an acceptable level

### Fonts

Well - default fonts are good but custom fonts are better (tm). So i use
the following fonts:

- Window Title: Fira Sans SemiBold 10
- Interface: Fira Sans Book 10
- Document: Roboto Slab Regular
- Monospace: Fira Mono for Powerline Regular 11

On the T440p Hinting Slight with Subpixel antialiasing works great at font
scaling factor of 1.00.

### Workspaces

No clue how people can work with the default settings of Gnome 3. Thankfully
the tweak tool offers some configuration.

- Dynamic workspaces huh? Disable that in gnome-tweak-tool and set it to use
  static if you ever want to have some organization wher to put stuff.
- I use 6 workspaces on the T440p - probably shitty for the more powerful
  XPS15 where i currently use a total of 16 with a 4x4 grid.

### Topbar

In the tweak tool there are some settings for the top bar.

- Battery percentage - well still very limited
- Show date, seconds and week numbers

### Windows and focus

Before Unity i used focus on hover which got killed by the global menu. Now
that the global menu is gone and probably not needed since most applications
now seem to have their stuff in the title bar instead of wasting veritical
space with a menu bar i am back to sloppy windows focusing which can be
enabled in the tweak tool.

Also i keep the titlebar buttons on the left - glad that this option is
possible in the tweak tool.

## Issues

- No fractional scaling with X11 and Gnome3 - My T440p has a 1080p screen,
  so no issue there - this will be an issue when i update the XPS 15 which
  has a 4K screen.
- Windows placement with Gnome3/Mutter is terrible - withing back the defaults
  from Compiz ...
- Workspaces suck, especially that they are only vertical. I am used to a 4x4
  workspace grid which is no longer possible. Sucks to have 16 vertical 
  desktops eh?
- Gnome3 takes a lot of memory - there are some memory leaks - not sure how
  much of a problem that becomes, but i strongly feel that a desktop env
  should not ever use 3GB of RAM or something.


## Huh?

Well today is Apri 7, so still 2 weeks or so until launch of Ubuntu 18.04 so
lets see if things become better.

All in all its pretty usable for now.



