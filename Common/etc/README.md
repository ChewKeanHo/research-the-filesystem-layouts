# `etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses runtime configuration files parsed by one or more programs
or applications. Depending on the design and deployment, this directory can
serve as a single unified configuration directory for many programs, or it can
serve a single program in a restricted environment (e.g., inside a sandbox).

It is **ALWAYS** to back up this directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

The use of `.d` configuration directory strategy also reduces the configuration
complexities and making maintainability easier by just updating 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples:

```
etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...
      ...
    ...
  ...

OR

etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
    ...
  ...
```
