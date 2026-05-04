# `/usr/local/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing programs' and applications' configuration
files to function properly faciliated mainly for maintaining UNIX BSD
filesystems inter-compatibilties. It is unused by the MacOS system operations.

All configurations here are available to all users.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

The use of `.d` configuration directory strategy reduces the configuration
complexities and making maintainability easier by just keeping 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples with and without using `trademark` directory:

```
/usr/local/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/usr/local/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
