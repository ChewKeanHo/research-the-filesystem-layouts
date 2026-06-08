# `lib`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses library files (e.g., C object and library files) for
software developers to integrate into their products and applications. This
follows the conventional C programming language model.

Most modern compiled languages (Go, Rust, Nim, Swift, Objective‑C) provide
plugin‑based integration that facilitates runtime linking of library files.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
lib/
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

lib/
  product/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
  ...
```
