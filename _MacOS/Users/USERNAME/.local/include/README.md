# `/Users/[USERNAME]/.local/include`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, inclusion files (e.g. C header files) for extending the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage. This means that the inclusion files in this directory only appears
specifically for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure software without requiring
`root` or administrator(s) account for installation affecting the entire OS.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel permission).

Generally, you **SHOULD** place your files here.

This directory is part of the `local domain`.

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
