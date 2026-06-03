# `/home/[USERNAME]/.cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing cache files from user-specific
programs and applications. Most UNIX and UNIX-like operating system (OS)s create
this directory as it is. Otherwise, modern OSes symlinked it to the
`/home/[USERNAME]/.local/var/cache` directory, a `.local` common directory for
consistency with the filesystem hierarchy standards.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Programs that used this directory **SHOULD** remove the cache files to avoid
data poisoning or corruption after use.

To symlink this directory to `/home/[USERNAME]/.local/var/cache` manually,
simply execute the following command:

```
# cd "$HOME"
$ mkdir -p "./.local/var/cache"
$ if [ -d "./.cache" ]; then do mv "./.cache/*" "./.local/var/cache/."; done
$ rm -rf "./.cache" &> /dev/null
$ sync .
$ ln -s "./.cache" "./.local/var/cache"
```
