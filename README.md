Asus Keyboard Backlight Control
===============================

A control script for the keyboard backlight of ASUS devices.

This should work on any laptop that controls it's keyboard
backlight with `/sys/class/leds/asus::kbd_backlight`, specifically
it was been shown to work on ASUS G75VW Laptops but it should work
on the Asus Zenbook UX31A and similar models too.

If you have any problem with permissions you'll have to run
`asuskblctl permissions` as root.

To avoid having to run this script manually after every boot, a systemd service
is provided with the Arch package, to enable it run:

    sudo systemctl enable asuskblperm.service

NOTICE
------

Mostly copied from
[nvidiablctl](https://github.com/guillaumezin/nvidiabl/blob/master/scripts/usr/local/sbin/nvidiablctl).

LICENSE
-------

    Copyright (c) 2014 Amadeus Folego <amadeusfolego@gmail.com>
    Based on the the backlight control script for nvidia:
    Copyright (c) 2009-2011 Guillaume Zin <guillaume.zin@gmail.com>
    Site: https://github.com/guillaumezin/nvidiabl

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.
