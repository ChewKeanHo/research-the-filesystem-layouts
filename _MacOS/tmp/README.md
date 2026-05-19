# `/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s temporary files and directory.
On many OSes design, this directory gets cleared and cleaned on boot up.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are available to all users.

Also, it is recommended to clean up the temporary files before **AND** after use
to avoid post-use blames or corrupted data usage.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/tmp/
  trademark/
    product/
      ...

OR

/tmp/
  product/
    ...
```
