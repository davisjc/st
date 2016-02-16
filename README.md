# st
simple terminal by [suckless](http://st.suckless.org), with some modifications.

What's Changed
------------
This is a fork of [st](http://st.suckless.org) with a few
[patches](http://st.suckless.org/patches/) applied:

* [scrollback + scrollback-mouse](http://st.suckless.org/patches/scrollback) patches
    * Shift + PGUP/PGDN scrolls buffer by page.
    * Shift + MWHEEL scrolls buffer line-by-line.
* [externalpipe](http://st.suckless.org/patches/externalpipe) patch
    * Grabs the buffer contents.
    * Map "Alt + u" for url launching with dmenu (see `config.h` for mapping).
      Currently, this is hardcoded to Google Chrome, but you can specify a different program in
      `config.h`.

Other changes:

* **Colors**
    * `config.h` has been changed a bit to reflect a custom color scheme
      (currently hbw's [Aurora](https://github.com/henrybw/vim-colors-aurora)).
* **Font**
    * I use the "Hack" font (also specified in `config.h`).

**NOTE:** `config.def.h` is the default, unmodified `config.h` for this particular build of st.
My changes can be inferred by comparing the two.  Also, I've included the patch files applied for
reference.

Dependencies
------------
* **xurls** - used to extract urls from the buffer
    * Available on Arch Linux via this [AUR package](https://aur.archlinux.org/packages/xurls/).
* **dmenu** - used to select a url from the extracted urls
    * Available in the community repo on Arch Linux.
* **Xlib headers** - required to build

Installation
------------
Run (as root, if necessary):

    make clean install

By default, st will be installed to `/usr/local`; this can be changed in `config.mk`.

Credits
-------
The original st project can be found [here](http://st.suckless.org).

Thanks to hbw for his colors.

