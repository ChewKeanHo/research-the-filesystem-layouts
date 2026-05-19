# `/Users/[USERNAME]/.local/include`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, inclusion files (e.g. C header files) for extending the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage. This means that the inclusion files in this directory only appears
specifically for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with the users'
customization. The secondary purpose is to facilitate a way to procure programs
and applications without using sysadmins or root account (e.g. `sudo`) that
affects the entire OS' security.

Generally, you **SHOULD** place your own custom inclusion files here. It
will be made available only for you.

All files here are available only to the owning user.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/Users/[USERNAME]/.local/include/
  trademark/
    product/
      lib1.h
      lib1_freebsd-amd64.h
      kernel8.h
      kernel8_freebsd-amd64.h
      ...

# OR

/Users/[USERNAME]/.local/include/
  product/
    lib1.h
    lib1_freebsd-amd64.h
    kernel8.h
    kernel8_freebsd-amd64.h
    ...
```
