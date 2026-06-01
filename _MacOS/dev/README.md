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

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications. For examples:

* ATA Hard disk (SATA) storage device can be repesented as:
    * `/dev/adaN` in `FreeBSD`.
    * `/dev/sdN` in `Linux`.
    * `/dev/diskN` in `MacOS`.
* Floppy Disk storage device can be repesented as:
    * `/dev/fdN` in `FreeBSD`.
    * `/dev/fdN` in `Linux`.
    * unsupported in `MacOS`.
* NVME storage device can be repesented as:
    * `/dev/ndaN` in `FreeBSD`.
    * `/dev/nvmeNnM` in `Linux`.
    * `/dev/diskN` in `MacOS`.
* Null device can be represented as:
    * `/dev/null` in `FreeBSD`.
    * `/dev/null` in `Linux`.
    * `/dev/null` in `MacOS`.
* SecureDigital (SD) or Multimedia Card (MMC) storage devices can be repesented
  as:
    * `/dev/cdN` in `FreeBSD`.
    * `/dev/mmcblkN` in `Linux`.
    * `/dev/diskN` in `MacOS`.
* Optical compat disc (CD) storage device can be repesented as:
    * `/dev/cdN` in `FreeBSD`.
    * `/dev/srN` in `Linux`.
    * `/dev/diskN`, `/dev/cdrom` as symlink in `MacOS`.
* SCSI Hard disk storage device can be repesented as:
    * `/dev/daN` in `FreeBSD`.
    * `/dev/sdN` in `Linux`.
    * `/dev/diskN` in `MacOS`.
* Strong randomness devices can be represented as:
    * `/dev/random` (high quality), `/dev/urandom` (regardless of entropy) in `FreeBSD`.
    * `/dev/random` (high quality), `/dev/urandom` (regardless of entropy) in `Linux`.
    * `/dev/random` (high quality), `/dev/urandom` (regardless of entropy) in `MacOS`.
* Tape storage device can be repesented as:
    * `/dev/saN` in `FreeBSD`.
    * `/dev/stN` in `Linux`.
    * unsupported in `MacOS`.
* USB serial device can be represented as:
    * `/dev/cuaUN` in `FreeBSD`.
    * `/dev/ttyUSBN` in `Linux`.
    * `/dev/cu.usbserial-NNNN`, `/dev/tty.usbserial-NNNN` in `MacOS`.
* USB storage device can be represented as:
    * `/dev/daN` in `FreeBSD`.
    * `/dev/sdN` in `Linux`.
    * `/dev/diskN` in `MacOS`.
