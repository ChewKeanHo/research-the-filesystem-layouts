# `/usr/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s temporary files and directory.
On many OSes design, this directory gets cleared and cleaned on boot up.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are available to all users and is restricted based on UNIX
filesystem permissions.

Also, it is recommended to clean up the temporary files before **AND** after use
to avoid post-use blaming or corrupted data usage.

On majority of Linux-based OSes, this directory replaces all other temporary
directory (e.g., `/var/tmp`, `/usr/tmp`). In some Linux-based OSes like
Red Hat Linux and Fedora, this directory is symlinked to `/tmp` directory,
a symlink to `/var/tmp` directory. In short, if `/tmp` is unavailable, look for
those 2 directories.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/tmp/
  trademark/
    product/
      ...

OR

/usr/tmp/
  product/
    ...
```
