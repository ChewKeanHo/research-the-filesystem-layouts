# `/usr/share/doc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing CPU architecture independent documentation
files (e.g. man pages, PDFs, etc) faciliated mainly for maintaining UNIX BSD
filesystems inter-compatibilties. It is unused by the MacOS system operations.

All files here are available to all users.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the documentation files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  share/
    doc/
      trademark/
        product/
          file1.pdf
          file2.txt
          ...

OR

/usr/
  share/
    doc/
      product/
        file1.pdf
        file2.txt
        ...
```
