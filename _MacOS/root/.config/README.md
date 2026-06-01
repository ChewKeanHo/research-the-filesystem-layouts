# `/root/.config`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing configuration files from
user-specific programs and applications. Most UNIX and UNIX-like OSes create
this directory as it is. Otherwise, modern OSes symlinked it to the
`/root/.local/etc` directory, a `.local` common directory for consistency with
the filesystem hierarchy standards.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

This directory is **ONLY** accessible `root` and OS administrators (users with
`wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

To symlink this directory to `/root/.local/etc` manually, simply execute the
following command:

```
# cd "$ROOT"
$ mkdir -p "./.local/etc"
$ if [ -d "./.config" ]; then do mv "./.config/*" "./.local/etc/."; done
$ rm -rf "./.config" &> /dev/null
$ sync .
$ ln -s "./.config" "./.local/etc"
```
