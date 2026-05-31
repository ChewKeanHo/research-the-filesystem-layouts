# `[APPNAME].app/Contents/Helpers`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an app's help resources (not help executable) data files.
For executables, place them inside `MacOS` directory instead.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
[APPNAME].app/Contents/Helpers/
  trademark/
    product/
      README.txt
      HOW-TO.txt
      DEBUG.txt
      ...

# OR

[APPNAME].app/Contents/Helpers/
  product/
    README.txt
    HOW-TO.txt
    DEBUG.txt
    ...
```
