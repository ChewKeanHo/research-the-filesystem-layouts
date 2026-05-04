# `/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing temporary files and directories faciliated
mainly for maintaining UNIX BSD filesystems inter-compatibilties. It is unused
by the MacOS system operations.

It is safe to assume that this directory gets cleared and cleaned on boot up.

All files and directories here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and after use to
avoid post-use blaming or corrupted data usage.

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

Here are the examples with and without using `trademark` directory:

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
