# My st (simple terminal) build

st is a simple terminal emulator for X which sucks less (st is created by the [suckless](https://suckless.org) team).  This is my personal build of st, based on DistroTube's build.  I used some patches in this build to make st more like myself.  The patches I added to this build include:
+ alpha+[focus](focus) (for transparency)
+ font2 (to allow setting more than one font, useful when the default font has missing glyphs)
+ scrollback (scrollback through terminal using Shift+PageUp/PageDown.)
+ scrollback mouse altscreen (allows scrolling using Shift+MouseWheel.)
+ dynamic-cursor-color (Swaps the colors of your cursor and the character you're currently on (much like alacritty).)

# How to install st?

Download the source code from this repository or, preferably, use a git clone:

	git clone https://github.com/tiagovercosa/st
	cd st
    sudo make clean install
	
NOTE: Installing st will overwrite your existing st installation so make a backup of your current config if you need.

Also, be sure to have a composite manager (`xcompmgr`, `picom`, `compton`, etc.) running if you want transparency, and the `mononoki Nerd Font` to properly render stuff.

# Small Note on Emojis and Special Characters

If st crashes when viewing emojis, install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) or [libxft-bgra-git](https://aur.archlinux.org/packages/libxft-bgra-git/) from the AUR.

Note that some special characters may appear truncated if too wide. You might want to manually set your emoji/special character font to a lower size in the `config.h` file to avoid this.
