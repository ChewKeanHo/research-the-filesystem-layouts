# `/Users/[USERNAME]/.local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user-specific system directory with its own
[Common](/Common) filesystems specifically for a user. This extends the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage.

The goal is to extend the complete OS for this specific user (e.g. his/her own
programs, configurations, etc) without affecting the OS' *Complete* system
functionalities. Different user has different `.local` configurations and the
OS will personalize for that user.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD AND EXTREMELY ENCOURAGED** to place your programs,
applications, and files here. All of them are only available for you and you
only. The sole reason with the split between the OS and your `.local` filesystem
is to ensure you **DO NOT** interfere with the OS at all while providing you
freedom to customize your experiences. Moreover, **this setup is ROOTLESS**
(does not need root or system adminstrators (sysadmin) privileges) so you know
your setup only affects YOU; not everyone using the OS or the OS itself.

On some Linux UNIX-like OSs notably SystemD-based, Red Hat, and Fedora; this
directory is heavily used as they shifted all user customizations into here with
dedicated software like rootless package manager (e.g. Flatpak -
`$ flatpak --user install`).

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When this directory combines with [Common](/Common) directories structure, it
houses user-only specific filesystems on top of the operating system (OS),
personalized it just for this user. The combination happens inside a `.local`
sub-directory of this directory. The commonly seen structures would be:

```
/Users/[USERNAME]/.local/
  bin/
  etc/
  include/
  lib/
  libexec/
  sbin/
  share/
  src/
  var/
```
