# `/home/[USERNAME]/.var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing user-only and user-specific
transient data files (e.g. log files, saved games, states files, data files).
Most UNIX and UNIX-like operating system (OS)s create this directory as it is.
Otherwise, modern OSes symlinked it to the `/home/[USERNAME]/.local/var`
directory, a `.local` common directory for consistency with the filesystem
hierarchy standards.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

To symlink this directory to `/home/[USERNAME]/.local/var` manually, simply
execute the following command:

```
# cd "$HOME"
$ mkdir -p "./.local/var"
$ if [ -d "./.var" ]; then do mv "./.var/*" "./.local/var/."; done
$ rm -rf "./.var" &> /dev/null
$ sync .
$ ln -s "./.var" "./.local/var"
```
