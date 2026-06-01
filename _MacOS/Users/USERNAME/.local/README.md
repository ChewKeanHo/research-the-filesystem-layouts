# `/Users/[USERNAME]/.local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user-specific system directory with its own
[Common](/Common) filesystems. This extends the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage.

The goal is to extend the complete OS for this specific user (e.g. his/her own
programs, configurations, etc) without affecting the OS' *Complete* system
functionalities. Different user has different `.local` configurations and the
OS will personalize for the specific user.

The main purposes are:

1. Extends the OS completeness to user's specific personalized configurations.
   Different user has different unique `.local` configurations.
2. Extends the personalization without affecting the OS' *Complete* system
   initialization.
3. Allows user to procure software without requiring `root` or administrator(s)
   account for installation that affects the entire OS (also known as
   `Rootless Install`).

On some Linux UNIX-like OSs notably SystemD-based, Red Hat, and Fedora; this
directory is heavily used as they shifted all user customizations into here with
dedicated software like rootless package manager (e.g. Flatpak -
`$ flatpak --user install`).

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD AND EXTREMELY ENCOURAGED** to place your programs,
applications, and files here. All of them are only available specifically for
you.

This directory is part of the `local domain`.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory itself is a [Common](/Common) directories structure. Hence, its
downstream can be as follows:

```
/Users/[USERNAME]/.local/
  bin/
  etc/
  include/
  lib/
  lib[ARCH]/
  libexec/
  sbin/
  share/
  src/
  var/
```
