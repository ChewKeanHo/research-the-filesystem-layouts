# `lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture specific library files (e.g compiled
linkable object files). These files are accessible by various programs,
applications, and development project for an unified repository management.

One should use this directory sparingly and should prioritize `lib` directory
instead. This pattern was conceived since the `x86` CPU was migrating from its
32-bits to 64-bits architectures extension (e.g. `lib32`). Many OSes are
dropping the use and instead use `[NAME]_[COMPILER]-[OS]-[ARCH].[EXT]` filename
pattern in the same library package.




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
