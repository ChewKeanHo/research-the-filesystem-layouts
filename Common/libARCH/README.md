# `lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU‑architecture‑specific library files for software
developers. It follows the same C‑language model as `lib/` but exists for
foreign architectures (e.g., `i386` libraries on an `amd64` OS) to support
inter‑CPU compatibility. This pattern was conceived during the migration from
`x86` to `x86_64` hardware, when both 32‑bit and 64‑bit libraries were still in
simultaneous use.

As of the year 2026, most CPUs have fully migrated to 64‑bit, so this directory
is rarely used. One should use it sparingly and prioritize `lib/` directory.
Many developers now use the triplet filename pattern:

`[NAME]_[COMPILER]-[OS]-[ARCH].[EXT]`

To use this directory, define `[ARCH]` according to the OS distributor's
definition list and the intended target. Consult the distributor's documentation
for specifics. For the `x86` in `x86_64` case, `32` was used as the value for
`x86`, so `lib32` is common in `FreeBSD` and `Linux`‑based OSes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
lib[ARCH]/
  trademark/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...
    ...
  ...

# OR

lib[ARCH]/
  product/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
  ...
```
