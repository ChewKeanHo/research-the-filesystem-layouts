# `/usr/include`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing inclusion files (e.g. C header files)
faciliated mainly for maintaining UNIX BSD filesystems inter-compatibilties. It
is unused by the MacOS system operations.

All files here are available to all users.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the inclusion files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  include/
    trademark/
      product/
        lib1.h
        lib1_freebsd-amd64.h
        kernel8.h
        kernel8_freebsd-amd64.h
        ...

# OR

/usr/
  include/
    product/
      lib1.h
      lib1_freebsd-amd64.h
      kernel8.h
      kernel8_freebsd-amd64.h
      ...
```
