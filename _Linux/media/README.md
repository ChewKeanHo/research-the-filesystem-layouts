# `/media`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all mounted removable media such as but not
limited to CD, floppy disks, USB storage devices, external disks, decrypted
partitions, or volume managed partitions.

Each first-level sub-directory holds a mounted device.

The rationale is to cater for one or more devices instead of queue-and-hold the
`/mnt` directory per device. This made `/mnt` a temporary mounting directory
only for sysadmins and root user to debug mountable transactions.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You can place files or directory in the media directory here in accordance to
the designated filesystem ownership and permissions.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `automount(8)` manual for specifications.

Each sub-directory holds a mounted device be it physical or virtual
(e.g. decrypted partitions). The first sub-directory layer is recommended to use
the device's hardware label for easier identifications. Otherwise, the hardware
UUID label is a good fallback.
