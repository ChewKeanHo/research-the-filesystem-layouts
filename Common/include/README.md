# `include`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses inclusion files (e.g., C header files) for software
developers to integrate into their products and applications. This follows the
conventional C programming language model, where each source code file (`.c`)
comes with a corresponding header file (`.h`). The header file declares
functions made available either from the source code or its compiled library
file (`.o`).

Modern programming languages such as Go, Rust, Nim, Swift, and Objective‑C no
longer use header files; therefore, they do not typically use this directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
include/
  trademark/
    product/
      lib1.h
      lib1_freebsd-amd64.h
      kernel8.h
      kernel8_freebsd-amd64.h
      ...
    ...
  ...

# OR

include/
  product/
    lib1.h
    lib1_freebsd-amd64.h
    kernel8.h
    kernel8_freebsd-amd64.h
    ...
  ...
```
