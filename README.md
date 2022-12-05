# vboxtools
my tools for Linux VBOX guests

This file is an LSB compatibale init file for vbox shared folder mounts.

It is written for Ubuntu distro. The lsb functions are in different places on Red Hat distros.  The log file message functions have different names on the different distros.

The mount points are hard coded to sit within a top level directory called /import. They will create sub folders called common and local; the share names set by the host must be common and local. 

Code for a third folder mounted in / has been commented out. It woulod be called /data and have the share name of data. 

The share names are held in the SHARES[*] array; the mount points held in the MOUNT[*] array. The list element must agree with the number of elements in both arrays.

./mountcommon and a service description file were added. I droped the need for a data and local system specific mount at this point. I also explored the use of alternative error message writers. 
