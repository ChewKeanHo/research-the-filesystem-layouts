# `/Users/[USERNAME]/.local/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, configuration files for extending the operating system's
functionalities from *Complete* stage to *Personalized* stage. This means that
configurations in this directory only appears specifically for this user.

Generally, you **SHOULD** place your own custom configuration files here. It
will be made available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

The use of `.d` configuration directory strategy reduces the configuration
complexities and making maintainability easier by just keeping 1 configuration
per file. Then, the program would loop through the directory and parse every
files to reconstruct the setup.

Here are the examples with and without using `trademark` directory:

```
/Users/[USERNAME]/.local/
  etc/
    trademark/
      product/
        settings.d/
          setting1.conf
          setting2.conf
          ...

# OR

/Users/[USERNAME]/.local/
  etc/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...
```
