# `/Users/[USERNAME]/.local/include`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific inclusion files (e.g. C header files) for extending the operating
system's functionalities from complete stage to personalized stage. This means
that configurations in this directory only appears specifically for this user.

Generally, you **SHOULD** place your own custom inclusion files here. It will be
made available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours. The
second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
/Users/[USERNAME]/.local/
  include/
    trademark/
      product/
        lib1.h
        lib1_freebsd-amd64.h
        kernel8.h
        kernel8_freebsd-amd64.h
        ...

# OR

/Users/[USERNAME]/.local/
  include/
    product/
      lib1.h
      lib1_freebsd-amd64.h
      kernel8.h
      kernel8_freebsd-amd64.h
      ...
```
