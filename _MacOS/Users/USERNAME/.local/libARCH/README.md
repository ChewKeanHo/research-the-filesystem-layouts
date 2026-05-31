# `/Users/[USERNAME]/.local/lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
CPU architecture specific library files (e.g. C object artifact files) for
extending the operating system (OS)'s functionalities from *Complete* stage to
*Personalized* stage. This means that the library files in this directory only
appears specifically for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure software without requiring
`root` or administrator(s) account for installation affecting the entire OS.

This directory pattern is considered old and obselete when `x86` CPU
architecture was migrated completely from `i386` to `amd64` architectures.
During the migrations, both architectures are required to exist so this pattern
was invented. Use unless absolutely necessary and only only place your own
system-wide custom CPU architecture specific library files here (e.g. `arm64`
library files on an `amd64` OS where they are used for cross-compilation).

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel permission).

Generally, you **SHOULD** place your files here.

This directory is part of the `local domain`.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples for ARCH is `32` (32-bit on 64-bit OS):

```
/usr/lib32/
  trademark/
    product/
      lib1.a
      lib1_freebsd-amd64.a
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/usr/lib32/
  product/
    lib1.a
    lib1_freebsd-amd64.a
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
