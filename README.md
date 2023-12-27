# Linux-Yoga-Pro-Slim-9i

Some troubles that I notice on yoga slim 9 linux.
I dualbooted w11 and arch.

## First noticeable problems

_1._ Keyboard not recognized by Xorg/Wayland display server;

_2._ Bass speakers do not work at all;

_3._ Some Key functions do not have any input;

_4._ Touchpad is usable only with the "right" pressure.

## Solutions

1. Keyboard not recognized by Xorg/Wayland display server:
    - Open /etc/default/grub, add i8042.dumbkbd to GRUB_CMDLINE_LINUX_DEFAULT="" like this: GRUB_CMDLINE_LINUX_DEFAULT="i8042.dumbkbd".
    - In the same file add i8042.dumbkbd=1 to GRUB_CMDLINE_LINUX="" like this: GRUB_CMDLINE_LINUX="i8042.dumbkbd=1"
    - Note that the Caps Lock LED stops turning on after this.
2. Bass speakers do not work at all:
