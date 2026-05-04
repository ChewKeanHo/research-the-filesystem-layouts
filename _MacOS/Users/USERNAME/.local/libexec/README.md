# `/Users/[USERNAME]/.local/libexec`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, non-user (e.g. daemon server) programs and applications for
extending the operating system's functionalities from *Complete* stage to
*Personalized* stage. This means that executables in this directory only
appears specifically for this user.

Generally, you **SHOULD** place your own custom programs and applications
here. It will be made available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

This directory **MUST NOT** have any sub-directory.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory for 32-bit
CPU Architecture (`lib32`):

```
/Users/[USERNAME]/.local/
  lib32/
    trademark/
      product/
        lib1.so
        lib1_freebsd-amd64.so
        kernel8.ko
        kernel8_freebsd-amd64.ko
        ...

# OR

/Users/[USERNAME]/.local/
  lib32/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...
```
