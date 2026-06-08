# `src`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses source files (e.g., C source files) for software
developers to integrate into their products. Following the conventional C model,
source code (`.c`) is readily available for import and can be compiled into
object files (`.o`).

All modern compiled languages such as Go, Rust, Nim, Swift, and Objective‑C use
this directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
src/
  trademark/
    product/
      lib1.c
      lib1_freebsd-amd64.c
      kernel8.c
      kernel8_freebsd-amd64.c
      ...
    ...
  ...

# OR

src/
  product/
    lib1.c
    lib1_freebsd-amd64.c
    kernel8.c
    kernel8_freebsd-amd64.c
    ...
  ...
```
