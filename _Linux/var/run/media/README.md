# `/var/run/media`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all mounted removable media such as but
not limited to CD, floppy disks, USB storage devices, external disks, decrypted
partitions, and volume group managed partitions.

The purpose is to cater for one or more devices differenciated from the
queue-and-hold `/mnt` directory per mount. `/media` is mainly for long lifetime
mounting while `/mnt` is for temporary mount mainly to debug the hardware or
filesystem.

The first-level sub-directory holds a mounted device.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In FreeBSD, this directory is unused and is facilitated via its `/media`
directory instead.

In majority of Linux-based OSes, this directory **IS REPLACED BY** `/media`
directory. For some like Red Hat Linux or Fedora, this directory was replaced by
`/var/run/media` directory instead.

In Apple `MacOS`, this directory is unused and is facilitated via its `/Volumes`
directory instead.

You can place files or directory in the media directory here in accordance to
the designated filesystem ownership and permissions.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `automount(8)` and `bsdisks(8)` manuals for specifications.

Each sub-directory holds a mounted medium be it physical device or virtual
managed partitions (e.g. decrypted paritions).

The first sub-directory layer is usually named as the device's hardware text or
partition UUID label for easy identifications.
