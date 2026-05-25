# `/root/.local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user-specific system directory with its own
[Common](/Common) filesystems specifically for a user. This extends the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage.

The goal is to extend the complete OS for `root` account without affecting the
OS' *Complete* system functionalities. It has its own `.local` configurations
and the OS will personalize for this account.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

**Only `root` and administrators (users with `wheel` permission) can access the
directory**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, unless absolute necessary, you **SHOULD NOT** place anything here
**UNLESS** you are the OS distributor. This is to avoid any conflict with the
upstream's registries that will break the OS in any way. Use `/home/[USERNAME]`
instead.

On some Linux UNIX-like OSs notably SystemD-based, Red Hat, and Fedora; this
directory is heavily used as they shifted all user customizations into here with
dedicated software like rootless package manager (e.g. Flatpak -
`$ flatpak --user install`).




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When this directory combines with [Common](/Common) directories structure, it
houses user-only specific filesystems on top of the operating system (OS),
personalized it just for this user. The combination happens inside a `.local`
sub-directory of this directory. The commonly seen structures would be:

```
/root/.local/
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
