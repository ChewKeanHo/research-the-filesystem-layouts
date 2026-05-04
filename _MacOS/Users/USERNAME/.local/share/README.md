# `/Users/[USERNAME]/.local/share`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific CPU architecture independent data files (e.g. fonts, pdfs, etc)
for extending the operating system's functionalities from complete stage to
personalized stage. This means that data in this directory only appears
specifically for this user.

Generally, you **SHOULD** place your own custom data here. It will be made
available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and applications
without using sysadmins or root account that affects the entire operating
system.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the data files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
/Users/[USERNAME]/.local/
  share/
    trademark/
      product/
        docs/
          README.pdf
          Terms-of-Service.pdf
          ...
        licenses/
          LICENSE.pdf
          LICENSE.txt
          LICENSE.html
        ...

# OR

/Users/[USERNAME]/.local/
  share/
    product/
      docs/
        README.pdf
        Terms-of-Service.pdf
        ...
      licenses/
        LICENSE.pdf
        LICENSE.txt
        LICENSE.html
      ...
```
