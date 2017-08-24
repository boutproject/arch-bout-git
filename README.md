Arch package for BOUT++
=======================

This contains a PKGBUILD file to build a package for Arch Linux
from the latest release in a the same way as packages in the AUR
https://wiki.archlinux.org/index.php/Arch_User_Repository .

Clone this repository and cd into it:

    $ git clone https://github.com/boutproject/arch-bout-git.git
    $ cd arch-bout-git

then run makepkg to fetch, compile and install BOUT++.

    $ makepkg -si

This should also make sure that the dependencies are installed.

After installation you should be able to run ``bout-config``,
which can be used to find BOUT++ components and build examples.

Some more information is in the BOUT++ user manual:

* http://bout-dev.readthedocs.io/en/latest/user_docs/makefiles.html

