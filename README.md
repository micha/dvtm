dvtm - dynamic virtual terminal manager
=======================================

dvtm brings dwm and it's concept of tiling window management to 
the console. See http://www.brain-dump.org/projects/dvtm for
the latest version.

**Micha's mods:** Swap adjacent windows (see *config.h* `swapprev` and
`swapnext`).

**Micha's config:** See the `micha` branch for Micha's *config.h* settings.

Requirements
------------
In order to build dvtm you will need:

 * libncurses or libncursesw for wide character support

Installation
------------
Edit config.mk to match your local setup (dvtm is installed into
the /usr/local namespace and links against libncursesw by default).

Afterwards enter the following command to build and install dvtm (if
necessary as root).

    make && make install

Running dvtm
------------
Just run dvtm from the console, redirect stderr to a file (just in
case something goes wrong you will see it there).

    dvtm 2> log

If you want to display a one line status bar you can create a named
pipe and pass it's name to dvtm via it's -s command line option.
Make sure that the pipe remains open until dvtm is closed, see the
included dvtm-status script as an example.

Configuration
-------------
The configuration of dvtm is done by creating a custom config.h
and (re)compiling the source code.
