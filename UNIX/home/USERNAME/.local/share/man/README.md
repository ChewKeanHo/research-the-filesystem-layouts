# `/home/[USERNAME]/.local/share/man`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user-specific, user supplied,
non-critical, CPU architecture independent manual files for extending the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `man(1)` manual for specification.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/home/[USERNAME]/.local/share/man/
  trademark/
    product/
      man1/
        amd64
        aarch64
        ...
      man2/
        amd64
        aarch64
        ...
      ...
    ...
  ...

OR

/home/[USERNAME]/.local/share/man/
  product/
    man1/
      amd64
      aarch64
      ...
    man2/
      amd64
      aarch64
      ...
    ...
  ...
```
