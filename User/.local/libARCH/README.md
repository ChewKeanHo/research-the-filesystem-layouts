# `.local/lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user-specific, user supplied,
non-critical, CPU architecture specific library files (e.g. C object artifact
files) for extending the operating system (OS)'s functionalities from *Complete*
stage to *Personalized* stage.

This directory pattern is considered old and obselete when `x86` CPU
architecture was migrated completely from `i386` to `amd64` architectures.
During the migrations, both architecture-specific libraries are required to
exist on an OS so this pattern was invented. Only place your files here (e.g.
`arm64` library files on an `amd64` OS where they are used for
cross-compilation) when absolute necessary.

This directory **MUST NOT** have any sub-directory.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples for ARCH is `32` (32-bit on 64-bit OS):

```
.local/lib[ARCH]/
  trademark/
    product/
      lib1.a
      lib1_freebsd-amd64.a
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

.local/lib[ARCH]/
  product/
    lib1.a
    lib1_freebsd-amd64.a
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
