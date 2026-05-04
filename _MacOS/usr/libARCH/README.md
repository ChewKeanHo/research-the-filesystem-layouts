# `/usr/libARCH`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing CPU architecture specific programs' and
applications' library files to function properly faciliated mainly for
maintaining UNIX BSD filesystems inter-compatibilties. It is unused by the MacOS
system operations.

All libraries here are available to all users.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory for 32-bits
libraries (`lib32`):

```
/usr/
  lib32/
    trademark/
      product/
        lib1.so
        lib1_freebsd-i386.so
        kernel8.ko
        kernel8_freebsd-i386.ko
        ...

# OR

/usr/
  lib32/
    product/
      lib1.so
      lib1_freebsd-i386.so
      kernel8.ko
      kernel8_freebsd-i386.ko
      ...
```
