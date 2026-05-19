# `/Users/[USERNAME]/.local/share/fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific font files for extending the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage. This means that
font files in this directory only appears specifically for this user.

Generally, you **SHOULD** place your own custom font files here.

All files here are available only to the owning user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

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
/Users/[USERNAME]/.local/share/fonts/
  trademark/
    product1/
      font1.tff
      LICENSE.txt
      ...
    product2/
      font2.tff
      LICENSE.txt
      ...
    ...

# OR

/Users/[USERNAME]/.local/share/fonts/
  product1/
    font1.tff
    LICENSE.txt
    ...
  product2/
    font2.tff
    LICENSE.txt
    ...
  ...
```
