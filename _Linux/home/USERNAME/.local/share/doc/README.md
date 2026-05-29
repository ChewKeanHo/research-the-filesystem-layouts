# `/home/[USERNAME]/.local/share/doc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific document files (e.g. man pages) for extending the operating
system (OS)'s functionalities from *Complete* stage to *Personalized* stage.
This means that font files in this directory only appears specifically for this
user.

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




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/home/[USERNAME]/.local/share/doc/
  trademark/
    product1/
      program.pdf
      program.txt
      program.1
      ...
    product2/
      program.pdf
      program.txt
      program.1
      ...
    ...

# OR

/home/[USERNAME]/.local/share/doc/
  product1/
    program.pdf
    program.txt
    program.1
    ...
  product2/
    program.pdf
    program.txt
    program.1
    ...
  ...
```
