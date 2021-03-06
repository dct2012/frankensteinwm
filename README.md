**THIS REPO IS ARCHIVED AND UNMAINTAINED**

4wm
=============
----------------------
**4wm** is a versatile, dynamic tiling and floating window manager with 
two borders. Its goal is to be versatile and simple. There are four modes: 
tiling, floating, monocle and video. There are four direction in which you can tile, four
directions in which a window can swap with another, and four directions in which you can 
resize a window. Each desktop can have gaps between windows and the size can be change. 
Each virtual desktop has its own properties, unaffected by other desktops' or monitors' 
settings.

Modes
-----

There are four modes: tiling, floating, monocle and video. 
* **Tiling**
  * Tiling mode has four directions it can tile: bottom, left, right, and top. In tile 
  mode, the current window will slpit and the new window will fill the half of which
  direction is currently selected.
* **Monocle**
  * Monocle is a fullscreen mode that respects the desktops' gaps and a screens' panel. 
* **Video**
  * Video is a fullscreen mode that ignores both the desktops' gaps and a screens' panel. 

This is a tiling window manager, so anytime a window is created, we tile/handle/manage it. 
The exception to the rule is in floating mode.

* **Floating**
  * In floating mode, the window will appear in the middle of the screen. You then manage it.
  If you drag it to a desktop that's in monocle or video mode, it'll be drawn as such.

In video and monocle mode, each window is handled like it is in the tiling mode; it only 
appears to be fullscreen. Meaning, the windows will be split and placed according to the
current direction, the window is only drawn in fullscreen.

Panel - Statusbar
-----------------

4wm does not provide a panel or statusbar. It provides a way to pipe the information to a
panel or statusbar. Currently, only [dzen2][dz2] is supported.

  [dz2]: https://github.com/robm/dzen

Menu - launcher
---------------

4wm provides a menu or a launcher similar to xmonad's grid select. It will use
the colors from your Xdefaults for the tiles. 

Installation
------------

You need xcb and xcb-utils then,
copy `config.def.h` as `config.h`
and edit to suit your needs.
Build and install.

    $ cp config.def.h config.h
    $ $EDITOR config.h
    $ make
    # make clean install

Notes
-----
    * Add the launch option -window to steam games.

Bugs
----

For any bug or request [fill an issue][bug] on [GitHub][ghp]. Also check the [TODO][tdo]
for your issue.

  [bug]: https://github.com/dct2012/4wm/issues
  [ghp]: https://github.com/dct2012/4wm
  [tdo]: https://github.com/dct2012/4wm#TODO


License
-------

Licensed under MIT/X Consortium License, see [LICENSE][law] file for more copyright and license information.

   [law]: https://raw.github.com/dct2012/4wm/master/LICENSE
 
Thanks
------

* [the suckless team][skls] for [dwm][] 
* [c00kiemonster][cookiemonster] for [monsterwm][]
* [Cloudef][cloudef] for [monsterwm-xcb][]
* [venam][vnm] for [2bwm][]
* Michael Stapelberg for [i3][]
* [moetunes][] for [dminiwm][]
* [pyknite][] for [catwm][] 


  [skls]: http://suckless.org/
  [dwm]:  http://dwm.suckless.org/
  [moetunes]: https://github.com/moetunes
  [dminiwm]:  https://bbs.archlinux.org/viewtopic.php?id=126463
  [pyknite]: https://github.com/pyknite
  [catwm]:   https://github.com/pyknite/catwm
  [monsterwm]: https://github.com/c00kiemon5ter/monsterwm
  [cookiemonster]: https://github.com/c00kiemon5ter
  [monsterwm-xcb]: https://github.com/Cloudef/monsterwm-xcb
  [cloudef]: https://github.com/Cloudef
  [2bwm]: https://github.com/venam/2bwm
  [vnm]: https://github.com/venam
  [i3]: http://i3wm.org/
