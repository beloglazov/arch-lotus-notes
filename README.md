# Lotus Notes on Arch Linux 32bit

This project contains a set of Shell scripts for installing Lotus Notes on Arch Linux 32bit. Since
some of the dependencies of Lotus Notes are only available from AUR, it is required to have `yaourt`
installed.

First of all, it is necessary to obtain Lotus Notes RPMs, which can be downloaded from IBM's web
site: http://www-01.ibm.com/software/lotus/products/notes/

The following RPMs should be placed into the cloned repository's root folder:

- ibm_lotus_activities-<version>.i586.rpm
- ibm_lotus_cae-<version>.i586.rpm
- ibm_lotus_feedreader-<version>.i586.rpm
- ibm_lotus_notes-<version>.i586.rpm
- ibm_lotus_sametime-<version>.i586.rpm
- ibm_lotus_symphony-<version>.i586.rpm

Where `<version>` is replaced by the actual version of Lotus Notes. The version number should be
written to the `notes-version` file, which is currently set to 8.5.3.

Then, you basically just need to run the following two scripts:

```Shell
./01-install-deps.sh
./02-install-notes.sh
```

The installation script also installs a GTK fix from https://github.com/sgh/lotus-notes_gtk2.23.3

Once the installation is completed, Lotus Notes can be started by running the `notes` script:

```Shell
./notes
```

To simplify the starting process, the `notes` scripts can be copied to `~/bin`, then Lotus Notes can
be started by simply executing:

```Shell
notes
```

More information on installing Lotus Notes on Arch Linux, including the 64bit version, can be found at https://wiki.archlinux.org/index.php/Lotus_Notes_in_32bit_Chroot


## License

The scripts are released under the Apache 2.0 license

Copyright (C) 2012 Anton Beloglazov
