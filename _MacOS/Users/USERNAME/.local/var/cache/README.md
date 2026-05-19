# `/Users/[USERNAME]/.local/var/cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific cache files for extending the operating system's functionalities
from *Complete* stage to *Personalized* stage. This means that data in this
directory only appears specifically for this user.

Generally, you **SHOULD** place your own cache files here. It will be made
available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/home/[USERNAME]/.local/var/
  cache/
    trademark/
      product/
        ...

# OR

/home/[USERNAME]/.local/var/
  cache/
    product/
      ...
```
