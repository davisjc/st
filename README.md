# st
simple terminal by [suckless](http://st.suckless.org), with some modifications.

What's Changed
------------
This is a fork of [st](http://st.suckless.org) with a few [patches](http://st.suckless.org/patches/) applied:

* [scrollback + scrollback-mouse](http://st.suckless.org/patches/scrollback) patches
    * shift + PGUP/PGDN scrolls buffer by page
    * shift + MWHEEL scrolls buffer line-by-line
* [externalpipe](http://st.suckless.org/patches/externalpipe) patch
    * grabs the buffer contents
    * map alt + u for url launching with dmenu (see `config.h` for mapping) currently, this is hardcoded to google chrome, but you can specify a different program in `config.h`
* [alpha](http://st.suckless.org/patches/alpha) patch
    * background translucency (requires a compositor; e.g., compton)

Other changes:

* **Colors**
    * `config.h` has been changed a bit to reflect a custom color scheme
* **Font**
    * i use the "hack" font (also specified in `config.h`)
* **Binds**
    * alt + u for opening urls via externalpipe

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

Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
The original st project can be found [here](http://st.suckless.org).
