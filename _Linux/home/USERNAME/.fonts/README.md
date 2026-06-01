# `/home/[USERNAME]/.fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing user-only and user-specific font
files. Most UNIX and UNIX-like operating system (OS)s create this directory as
it is. Otherwise, modern OSes symlinked it to the
`/home/[USERNAME]/.local/share/fonts` directory, a `.local` common directory for
consistency with the filesystem hierarchy standards.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

To symlink this directory to `/home/[USERNAME]/.local/share/fonts` manually,
simply execute the following command:

```
# cd "$HOME"
$ mkdir -p "./.local/share/fonts"
$ if [ -d "./.fonts" ]; then do mv "./.fonts/*" "./.local/share/fonts"; done
$ rm -rf "./.fonts" &> /dev/null
$ sync .
$ ln -s "./.fonts" "./.local/share/fonts"
```
