# `Common` Filesystem Layout

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This layout is used across various filesystem layers of OS, project repository
filesystem, and package filesystem architecture. These were abstracted from all
major OSes like `FreeBSD`, `Linux`-based OSes (consolidation of `SystemD`,
`FreeDesktop.org`, `Red Hat Linux`, `Debian`, `Devuan`, `Void Linux`, `Fedora`),
and Microsoft `Windows`.

For Microsoft `Windows`, due to its design and absence of its filesystem
hierarchy standards, the `Common` layout is mainly focused on deployment rather
than modifying the OS itself.

Each filesystem layer can selectively remove directory that obstructs its
objectives. For example:

* In `FreeBSD` and `Linux`-based OSes `Layer-1` filesystem, it rejects
  `include/`, `src/`, and `share/` directories intentionally as they are unused
  and burdening the boot speed for early directory scans.
* In `FreeBSD` and `Linux`-based OSes `Layer-2` filesystem and `Layer-3`
  filesystem, they reject `tmp/` and `var/` directories due to duplicated
  confusing roles. Hence, only `Layer-1` filesystem’s `tmp/` and `var/`
  directories are used.
* In `FreeBSD` and `Red Hat Linux` OSes `Layer-3` filesystem, they are still
  using `etc/` (`/usr/local/etc`) directory while others do not.




## Understanding The 4 Stages of Powering Up

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Generally, any OS (including Microsoft `Windows`) go through 4 stages:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. The goal varies but usually about OS self-rescue, boot
   selections, self-auditing, low-resources environment operations (e.g.
   embedded. This stage only uses `Layer-1` directories which are:
   * Root (`/`) directory - for `UNIX`-based OSes like `FreeBSD`, and
     `Linux`-based OSes.
   * Windows (`[DRIVE]/Windows`) directory - for Microsoft Windows.
2. **Full Catalogue** - focuses on extending the OS functionalities upto its
   distributor's designed full potentials. The goal is to extend the OS
   capabilities to the full functionalities warranted by the OS designer. This
   stage only uses `Layer-2` directory which is:
   * `/usr` directory - for `UNIX`-based OSes like `FreeBSD`, and `Linux`-based
     OSes.
3. **Complete** - focuses on extending the OS functionalities further with
   user's localized system-wide capabilities. The goal here is to extend the
   OS capabilities further to cater user's system-wide customized
   functionalities. This state only uses `Layer-3` directories which are:
   * `/usr/local` directory - for `UNIX`-based OSes like `FreeBSD`, and
     `Linux`-based OSes.
   * `/Libraries` and `/Applications` - for Apple's `MacOS`.
   * `[DRIVE]/Program Files` and `[DRIVE]/Program Files (x86)` - for Microsoft
     `Windows`.
4. **Personalized** - focuses on extending the OS functionalities specifically
   for a user. The goal here is to further customize the OS capabilities
   specifically for an user. This stage can revert back and forth with
   *Complete* stage whenever an user logged in or out of a session. This stage
   only uses `Layer-4` directories are:
   * `/home/[USERNAME]/.local` directory - for `UNIX`-based OSes like `FreeBSD`,
     and `Linux`-based OSes.
   * `/Users/[USERNAME]/Libraries` and `/Users/[USERNAME]/Applications` - for
     Apple's `MacOS`.
   * `[DRIVE]/Users/[USERNAME]/AppData` and `[DRIVE]/Users/[USERNAME]/.local` -
     for Microsoft `Windows`.

> [!NOTE]
>
> Most proprietary OSes notably Apple's `MacOS` and Microsoft `Windows` skip the
> **Full Catalogue** stage as they are not facing the open-source multiple
> distributors fragmentations like the open source OSes (e.g. `FreeBSD` and
> `Linux`-based OSes).




## Best Practices

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is **ALWAYS A GOOD PRACTICE (but not a rule)** to use `[trademark]-[product]`
naming pattern as shown above for avoiding naming collision (e.g.
`chewkeanho-date` from locally built program versus `date` from OS distributor's
supplied program). These have various advantages:

1. Locally developed/installed programs will not interfere with OS distributor's
   supply chains and causing confusion.
2. Both local developers and OS distributor can independently and happily
   control their development instead of forcing local developers to register the
   names with OS distributor which can be very burdening especially for
   open-source OSes like `FreeBSD` and `Linux`-based OSes.

For configuration-based directory, the UNIX-OSes' `.d/` config directory
strategy is great for:

1. solving the big, fat and complex single configuration file problem which
   always complicate encoding-decoding parser’s algorithms; AND
2. facilitating human and automation reliable updates since 1 configuration file
   is 1 setting. It is far less probability to make a mistake; AND
3. keeps the encoding-decoding parser’s algorithm extremely easy to maintain.
   Program would have just loop through the entire directory and use a 1 pattern
   to parse the configurations.




## Using As Project Repository

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This layout is **DEFINITELY APPLICABLE** for project repository layout (e.g.
`git` project repository). However, do keep in mind to **USE IT AS A REFERNECE;
NOT A RULE**.

Likewise, one can decide which directory to use or otherwise. Recommended
minimalistic layout is:

```
[PROJECT]/
  .git/                        # git's version control system.
    ...
  .gitignore                   # git's ignored files
  .gitmodules                  # git's submodules list
  .github/                     # GitHub interfacing configurations directory.
    ...
  .gitlab/                     # GitLab interfacing configurations directory.
    ...
  .internals/                  # repository's internal directory.
    ...
  AI_DECREES.md                # artificial intelligences deployment statements.
  CITATION.cff                 # academia citation metadata file.
  CODE_OF_CONDUCT.md           # project governance code of conduct legal file.
  CONTRIBUTING.md              # contributing policy file.
  CONTRIBUTORS.txt             # consolidated list of contributors (license).
  CREATORS.txt                 # consolidated list of authors (license).
  LICENSE.txt                  # copyright license file (using consolidated alias).
  MAINTAINERS.md               # project maintainers handbook.
  REFERENCES.md                # external references.
  SECURITY.md                  # project security policy.
  bin/                         # compiled exportable libraries. Add to `.gitignore`.
    ...
  etc/                         # Runtime configurations. Add to `.gitignore` and backup.
    ...
  include/                     # resources inclusion files.
    ...
  lib/                         # compiled exportable libraries. Add to `.gitignore`.
    ...
  src/                         # source files here.
    entities/                  # recommend: VIPER architecture.
      ...
    interactors/
      ...
    presenters/
      ...
    routers/
      ...
    views/
      ...
  share/                       # resources source files.
    fonts/                     # font files.
      ...
    doc/
      license/                 # license data files.
        ...
      ...
    locale/                    # i18n data files.
      ...
    man/                       # UNIX manual files.
      ...
    misc/
      ...
  tmp/                         # temporary workspaces. Add to `.gitignore`.
    ...
  var/                         # Runtime data. Add to `.gitignore` and backup.
    cache/                     # local cache files. Add to `.gitignore`.
      ...
    db/                        # local databases.
      ...
    log/                       # local log files.
      ...
```




## Using As Package Bundle

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This layout is **DEFINITELY APPLICABLE** for the data section of package design.
Keep in mind to **USE IT AS A REFERNECE; NOT A RULE**.

Likewise, one can decide which directory to use or otherwise. The design here
considered both single bundle deployment method (e.g. Apple/Microsoft package
bundle) and unpacking deployment method (e.g. `FreeBSD` and `Linux`-based
packages). The recommended minimalistic layout is:

```
[PACKAGE]{.tar.*z}.manifest.cert # [OPTIONAL] store manifest cryptographic signature.
[PACKAGE]{.tar.*z}.manifest      # [OPTIONAL] store manifest.
[PACKAGE]{.tar.*z}.cert          # package cryptographic signature.
[PACKAGE]{.tar.*z}/              # tar.*z archive+compress capable.
  Manifests/                     # package manifest (design your own).
    Base                         #   unpacking base directory (`/`, `/usr`, ...).
    Description/                 #   package long description.
      en                         #     package long description in english.
      zh-Hans                    #     package long description in simplified chinese.
      ...
    Name/                        #   package names in multiple languages.
      en                         #     package name in english.
      zh-Hans                    #     package name in simplified chinese.
      ...
    ID/                          #   package (product) IDs.
      SKU
      UUID
      DOI
      ISBN
      ...
    Packager/
      Version                    #   packager/unpack format version.
    Pitch/                       #   package one-liner's pitch.
      en                         #     package one-liner's pitch in english.
      zh-Hans                    #     package one-liner's pitch in simplified chinese.
      ...
    Version                      #   package version.
    ...
  Entitlements/                  # privacy manifest (design your own).
    Filesystem
    Camera
    Microphone
    ...
  ...                            # reserved for future packager development.
  Resources/                     # payload data directory.
    bin/                         # compiled executable binaries.
      ...
    etc/                         # resources configuration files.
      ...
    include/                     # resources inclusion files.
      ...
    lib/                         # compiled exportable libraries.
      ...
    libexec/                     # compiled non-commandable executable binaries.
      ...
    sbin/                        # compiled sysadmins executable binaries.
      ...
    src/                         # source file.
      ...
    share/                       # resources source files.
      ...
```
