# n411z-fixed-dsdt

Fixed Differentiated System Description Table (DSDT) for the Dell Inspiron N411Z for working Linux backlight hotkey. 

### I made this fix as a workaround for the limitation described at: https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1435039

The bug prevents the use of backlight hotkeys of the Dell Inspiron N411Z laptop. Turns out this was due to Dell making a syntax error at EisaId ("PNP0C0F") of the DSDT table before compilation using Intel IASL. See dsdt.txt for a decompiled version of the dsdt and do a diff against your own stock DSDT file to see differences.

See https://wiki.archlinux.org/index.php/DSDT#Compiling_into_the_kernel for instructions on how to compile dsdt.aml into your next Linux Kernel and backlights should be fully functional without any further modification.

See config folder for .kext fixes for running a Hackintosh using OSx86 on the N411Z.
