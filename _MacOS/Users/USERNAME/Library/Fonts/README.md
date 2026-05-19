# `/Users/[USERNAME]/Library/Fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing user-specific font files.

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain`.

Only admin-privileged (`wheel`) and owning users can access this directory.

You **CAN AND SHOULD** place or modify any files and folders manually.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/Users/[USERNAME]/Library/Fonts/
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

/Users/[USERNAME]/Library/Fonts/
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
