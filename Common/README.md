# Common Filesystem Layout

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The is the filesystem layout commonly used across each layers and across all
known operating system (OS)s, abstracted based on all the datasets available
here. Each directory has its vital role regardless of its layer's objectives.

Each filesystem layer can selectively remove directory that obstructs its
objectives. Examples:

* `Layer-1` UNIX-based OSes rejected `include`, `src`, `share` intentionally
  since they are unused and occupy resources (slowing down boot time) during its
  OS `Critical & Minimal` boot up stage.
* `Layer-2` and `Layer-3` UNIX-based OSes rejected both `tmp` and `var` due to
  duplicated roles. Hence, only `Layer-1`'s `/tmp` and `/var` are used.
* `Layer-3` for some UNIX-based OSes (notably FreeBSD and Red Hat Linux) still
  use `etc` (`usr/local/etc`) while others do not.




## Understanding The 4 Stages of Powering Up

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Generally, any OS (including Microsoft `Windows`) go through 4 stages:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. The goal varies but usually about OS self-rescue, boot
   selections, self-auditing, low-resources environment operations (e.g.
   embedded. This stage only uses the Root (`/`) directory called `Layer-1`.
2. **Full Catalogue** - focuses on extending the OS functionalities upto its
   distributor's designed full potentials. The goal is to extend the OS
   capabilities to the full functionalities warranted by the OS designer. This
   stage only uses `/usr` directory called `Layer-2`.
3. **Complete** - focuses on extending the OS functionalities further with
   user's localized system-wide capabilities. The goal here is to extend the
   OS capabilities further to cater user's system-wide customized
   functionalities. This stage only uses `/usr/local` directory called
   `Layer-3`.
4. **Personalized** - focuses on extending the OS functionalities specifically
   for a user. The goal here is to further customize the OS capabilities
   specifically for an user. This stage can revert back and forth with
   *Complete* stage whenever an user logged in or out of a session. This stage
   only uses `${HOME}/.local` directory called `Layer-4`.

> [!NOTE]
>
> Most proprietary OSes notably Apple's `MacOS` and Microsoft `Windows` skip the
> **Full Catalogue** stage as they are not facing the open-source multiple
> distributors fragmentations like the open source OSes (e.g. `FreeBSD` and
> `Linux`-based OSes).




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
[PACKAGE]{.tar.*z}.manifest.cert # [OPTIONAL] store manifest cryptographic signed signature.
[PACKAGE]{.tar.*z}.manifest      # [OPTIONAL] store manifest.
[PACKAGE]{.tar.*z}.cert          # package cryptographic signed signature.
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
  ...                            # reserved for future packager developemnt.
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
