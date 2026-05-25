# `/boot/efi`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing critical bootloading programs, applications,
and configuration files to initialize the operating system (OS) using
Unified Extensible Firmware Interface (UEFI), a successor to
Extensible Firmware Interface (EFI), with a single boot standards across
multiple CPU architectures such as but not limited to `i386`, `amd64`, `arm`,
`arm64`, and `risv`. This partition, called EFI System Partition (ESP), has
specific rules where it **MUST** be:

1. Hardware supporting UEFI boot; AND
2. is the **first** partition (as close to `0x0` address as possible); AND
3. `FAT32` format without any extra features; AND
4. `MSDOS_SUPER_MAGIC` flag enabled; AND
5. is `Primary` partition; AND
6. Minimum `512MB`; AND
7. UEFI firmware must be locatable complying to a set of hard-coded pathing
   (refer below); AND
8. Pathing are case insensitive (UPPERCASE is equal to lowercase); AND
9. Partition scheme as shown below; AND
   * **`GPT`**: ESP ID = `C12A7328-F81F-11D2-BA4B-00A0C93EC93B`; OR
   * **`MBR`**: ESP ID = `0xEF`.

> [!NOTE]
>
> For setting `boot` flag as `enabled`, it is **NOT** a requirement but to
> support legacy boot systems (e.g. BIOS boot for `i386` and `amd64` CPU
> architectures).

The goal is plain simple: boot up the OS with a hardware-software matching boot
configurations, initialize kernel until the OS can take over for achieving
`Minimal & Critical` functionalities stage.

Generally, you **SHOULD ONLY** place EFI bootloading programs and their
configuration files inside this directory. Due to early boot sequences are
hardware specific which can be very complex yet critical, this directory is
often housing the bootloading artifacts reliably and systematically generated
from the higher OS' functionalities.

This directory is the legacy mount point for the EFI boot partition. In some
UNIX-Like OS notably SystemD implementations, this directory is no longer used
and is replaced by `/efi` or `/boot` entirely instead. According to their
specifications, tools will look for this directory as a fallback after searching
for `/efi`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The universal path is a set of hard-coded UEFI bootable image file hard-coded
as follows based on the supported CPU architectures. Also, A lot of OSes usually
use the universal UEFI image files and then chain-load to their respective
OS-specific UEFI bootloader for hardware-software de-coupling maintenance sakes.
Moreover, to implement SecureBoot, a lot of OSes uses a `shim.efi` layer for
facilitating local machine owning key signing mechanism.

The following directory structure are known implementations:

```
/boot/efi/
  boot/
    BOOTX64.EFI                            # universal loader for `amd64`
    BOOTARM.EFI                            # universal loader for `arm`
    BOOTAA64.EFI                           # universal loader for `arm64`
    BOOTIA32.EFI                           # universal loader for `i386`
    BOOTRISCV64.EFI                        # universal loader for `riscv`
    dragonfly/
      LOADER.efi                           # DragonFly loader
    debian/
      GRUBX64.efi                          # Debian Grub2 bootloader
    elilo/
      ELILO.efi                            # ELILO bootloader
    fedora/
      GRUBX64.efi                          # Fedora Grub2 bootloader
    freebsd/
      LOADER.efi                           # FreeBSD loader
    haiku/
      HAIKU_LOADER.efi                     # Haiku loader
    microsoft/
      boot/
        bootmgfw.efi                       # Microsoft Windows Boot Manager
    netbsd/
      LOADER.efi                           # NetBSD loader
    openbsd/
      LOADER.efi                           # OpenBSD loader
    reactos/
      BOOTX64.efi                          # Reach OS loader
    redox/
      REDOX_LOADER.efi                     # Redox OS loader
    refind/
      REFIND_X64.efi                       # rEFInd bootloader
    solaris/
      LOADER.efi                           # Solaris loader
    systemd/
      SYSTEMD-BOOTX64.efi                  # SystemD bootloader
    openindiana/
      LOADER.efi                           # Illumos loader
    ubuntu/
      GRUBX64.efi                          # Ubuntu Grub2 bootloader

/System/Library/CoreServices/
  BOOT.efi                                 # Apple `MacOS` loader
```
