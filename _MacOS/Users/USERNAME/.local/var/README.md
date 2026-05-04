# `/Users/[USERNAME]/.local/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific transient variable data files (e.g. game saves, web server files,
etc) for extending the operating system's functionalities from complete stage
to personalized stage. This means that executables in this directory only
appears specifically for this user.

Generally, you **SHOULD** place your own custom data here. It will be made
available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the data files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
/Users/[USERNAME]/.local/
  var/
    trademark/
      product/
        log/
          access.log
          info.log
          ...
        cache/
          icons/
            banner_1200x1200.svg
            ...
        ...

# OR

/Users/[USERNAME]/.local/
  var/
    product/
      log/
        access.log
        info.log
        ...
      cache/
        icons/
          banner_1200x1200.svg
          ...
      ...
```
