# `/dev`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all device nodes (special files).

The goal is simple: the operating system (OS) maps all the device nodes by
kernel into the filesystem for hardware-software interactions.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the FreeBSD handbook for the device nodes definitions. For
examples:

* ATA Hard disk (SATA) storage device can be repesented as:
    * `/dev/adaN` in `FreeBSD`.
* Floppy Disk storage device can be repesented as:
    * `/dev/fdN` in `FreeBSD`.
* NVME storage device can be repesented as:
    * `/dev/ndaN` in `FreeBSD`.
* Null device can be represented as:
    * `/dev/null` in `FreeBSD`.
* SecureDigital (SD) or Multimedia Card (MMC) storage devices can be repesented
  as:
    * `/dev/cdN` in `FreeBSD`.
* Optical compat disc (CD) storage device can be repesented as:
    * `/dev/cdN` in `FreeBSD`.
* SCSI Hard disk storage device can be repesented as:
    * `/dev/daN` in `FreeBSD`.
* Strong randomness devices can be represented as:
    * `/dev/random` (high quality), `/dev/urandom` (regardless of entropy) in `FreeBSD`.
* Tape storage device can be repesented as:
    * `/dev/saN` in `FreeBSD`.
* USB serial device can be represented as:
    * `/dev/cuaUN` in `FreeBSD`.
* USB storage device can be represented as:
    * `/dev/daN` in `FreeBSD`.
