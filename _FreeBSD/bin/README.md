# `/bin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical programs and applications of an
operating system (OS) to function properly and minimally without any mounting
(e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for functionalities extension, performing self-rescue, or
straight up operational in resources constraint environment such as but not
limited to OpenWRT embedded router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer seeing performance compromise between
`/` and `/usr`, this directory is being symbolic linked to `/usr/bin` instead;
unifying both directories. This reduces the separation complexities while
simplifying the package managements to target `/usr/bin` only. **FreeBSD
however, have not seen to perform such implementation yet likely for backward
compatibility purposes.**

Generally, you **SHOULD ONLY** place programs that are very critical at early
booting stage without conflicting with existing POSIX compliant programs. In the
case of `/bin` being symbolic linked to `/usr/bin`, you **MUST NOT** place
anything here and use `/usr/bin` exclusively instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

All POSIX compliant registered programs based on IEEE POSIX1.0 list
(refer: https://pubs.opengroup.org/onlinepubs/9799919799/idx/utilities.html).
Among the known ones are:

```
[        - program to test a condition (used in shell scripting).
cat      - program to concatenate files to standard output.
chgrp    - program to change file group ownership.
chmod    - program to change file access permissions.
chown    - program to change file ownership and group.
cp       - program to copy files and directories utility.
date     - program to print and set datetime.
dd       - program to duplicate raw input/output.
df       - program to report filesystem and disk space capacity.
dmesg    - program to print or control kernel message buffers.
echo     - program to display content.
false    - program to do nothing or unnecessfully.
hostname - program to show OS's hostname.
kill     - program to kill a process.
ln       - program to make link in filesystem.
login    - program to login.
ls       - program to list item in filesystem.
mkdir    - program to make directory.
mknod    - program to make block or character special files.
more     - program to page through text.
mount    - program to mount a filesystem.
mv       - program to move things in filesystem.
ps       - program to report process status.
pwd      - program to report current directory location.
rm       - program to remove item in filesystem.
rmdir    - program to remove empty directory in filesystem.
sed      - program to stream and edit files in filesystem.
sh       - program to execute POSIX compatible shell.
stty     - program to configure terminal settings.
su       - program to change runtime user ID.
sync     - program to flush buffers in filesystem.
test     - program to test a condition.
true     - program to do nothing successfully.
umount   - program to unmount a filesystem.
uname    - program to report OS system information.
```

Optional programs (for more robust critical functionalities) are:

```
tar      - program to archive a directory.
cpio     - program to archive a directory.
gzip     - program by GNU for compression.
gunzip   - program by GNU for de-compression.
zcat     - program by GNU for de-compression.
netstat  - program to report network statistics.
ping     - program to perform ICMP network testing.
```
