# The Filesystem Hierarchy Layouts | (Holloway) Chew, Kean Ho's Knowledge Research

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Having trouble working with filesystems hierarchy layouts especially those that
has standardized regulations like UNIX and Windows? Are you looking for some
design references that are comforming and portable to as many operating as
possible? This is the right research dataset.

At (Holloway) Chew, Kean Ho's The Filesystem Hierarchy Layouts Research Project,
tech volunteers and me are continuously updating this repository for abstracting
common filesystems and directory layouts for various purposes. The research
goals are simple:

1. **Maximizing Compatibilities, Minimizing Conflicts** - analyzes and abstracts
   various standards for common patterns. Through these patterns, new projects
   can maximize inter-compatibilities and minimizing conflicts across multiple
   operating systems; AND
2. **Unifying Filesystems** - With common patterns in filesystems and directory
   organizations, packaging software for end-user can be simplified and unified
   for easier and maintainable maintenances works, automations, documentations,
   and communitions sakes; AND
3. **Solid and Hygienic Design References For Project Structuring** - something
   clean and reliable to refer (not a rule to enforce) when designing a project
   directory layout.

This dataset is a 100% deterministic with futuristic directive concequencies.
It is **100% human-made. Direct artificial intelligences (A.I) contributions
(e.g. vibe coding) IS STRICTLY PROHIBITED**. Only use A.I. for
non-concequential tasks like scouting for data source materials across the
broken search engines.

> [!WARNING]
>
> **REMEMBER: THESE ARE DESIGN REFERENCES; NOT RELIGIOUS RULES**. In other
> words, they are **opinions**.
>
> **DO NOT ATTEMPT TO RELIGIOUSLY ENFORCE** your project layouts by pointing
> back to this project. **IN NO WAY** this project is encourages anyone to
> adhere opinions.
>
> **Fanaticism destroys**. Please act responsbily and sensibly.

To use this dataset, first setup the markdown rendering `git` repository
(e.g. its GitHub mirror:
https://github.com/ChewKeanHo/research-the-filesystem-hierarchy-layouts). There
you can read the descriptions of each directory. For dataset, you need an UNIX
program called `tree`. Then execute the command:

```
$ tree -a -d path/to/TARGET/
```

The final outputs are consolidated into:

* **Common Directory Structure** - the [/Common](/Common). This is used for all
  common functioning directories that can combine with other directories for
  inter-compatible interpretations.
* **User Home Directory Structure** - the [/User](/User). This is used to setup
  an user's home directory especially for graphical user interface. It can
  combine with other directories for inter-compatible interpretations.
* **UNIX Filesystems Hierarchy** - the [/UNIX](/UNIX). The abstracted compatible
  filesystems across ALL UNIX OSes including BSD and Linux-based.

Any specific filesystem hierarchies are prefixed with an underscore (`_`). These
are dedicated directories for consolidating their respective specific designs
prior to `/UNIX` abstractions. Among them are:

* **FreeBSD Filesystems Hierarchy** - the [/_FreeBSD](/_FreeBSD) UNIX-like OS.
* **Linux Filesystems Hierarchy** - the [/_Linux](/_Linux)-based UNIX-like OS.
  Note that this consolidates all kinds of Linux-based OSes including but not
  limited to SystemD, FreeDesktop.org, Red Hat, Debian, Devuan, Void Linux,
  Fedora, etc.
* **Project Directory Structures** - the [/_Project](/_Project) commonly used
  for small modular project repository (e.g. `git` project repository).




## Design Sources & References

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Currently, this project had already processed the following engineering
specifications to match the outputs:

1. FreeBSD, 2025, "3.5. Directory Structure", *FreeBSD Handbook*, 4th Edition,
   The FreeBSD Project by The FreeBSD Community & The FreeBSD Foundations,
   viewed 09 December 2025, available at:
   https://docs.freebsd.org/en/books/handbook/basics/#dirstructure
2. Software Freedom Conservancy, 2025, "file-hierarchy — File system hierarchy overview",
   FreeDesktop via Software Freedom Conservancy, viewed 09 December 2025,
   available at:
   https://www.freedesktop.org/software/systemd/man/latest/file-hierarchy.html
3. FreeDesktop Filesystem Hierarchy Standard Project Contributors,
   The Linux Foundation, Daniel Quinlan, Paul 'Rusty' Russell, Christopher Yeoh;
   2025; "Filesystem Hierarchy Standard"; FreeDesktop via Software Freedom
   Conservancy; viewed 09 December 2025; available at:
   https://specifications.freedesktop.org/fhs/latest/rootFilesystem.html
4. GoHugo Authors; 2025; "Directory Structure"; The GoHugo Team; viewed
   09 December 2025; available at: https://gohugo.io/getting-started/directory-structure/
5. Palebloodsky; 2025; "Filesystems"; OpenWRT.org; viewed 09 December 2025;
   available at:
   https://openwrt.org/docs/guide-user/storage/filesystems-and-partitions
6. bxbzq, Cath O'Deray, kpedersen; 2021;
   "What's the proper way to install truetype fonts"; the FreeBSD Forum;
   The FreeBSD Foundation via XenForo Ltd; viewed 09 December 2025; available at:
   https://forums.freebsd.org/threads/whats-the-proper-way-to-install-truetype-fonts.79999/
7. Graham Perrin, David Edmundson; 2024; "Bug 442976"; bugs.kde.org; KDE.org;
   viewed 09 December 2025; available at: https://bugs.kde.org/show_bug.cgi?id=442976
8. Joe Brockmeier; 2025; "Debian Technical Committee overrides systemd change";
   *Articles*; lwn.net via Eklektix, Inc.; viewed 09 December 2025; available at:
   https://lwn.net/Articles/1041316/
9. rfc1036 et al.; 2025; "/var/lock/ is the standard interface for locks of serial devices";
   GitHub via GitHub.Inc; viewed 09 December 2025; available at:
   https://github.com/systemd/systemd/issues/38563
10. Devuan; 2025; "Welcome to Devuan"; Devuan.org; viewed 09 December 2025;
    available at: https://www.devuan.org/
11. Void Linux Contributors and Juan RP; 2025; "The Void (Linux) distribution";
    VoidLinux.org; viewed 09 December 2025; available at:
    https://docs.voidlinux.org/about/index.html
12. SystemD; 2025; "The Case for the /usr Merge"; SystemD.org; viewed
    09 December 2025; available at: https://systemd.io/THE_CASE_FOR_THE_USR_MERGE/
13. Oracle; 2012; "User Environment Feature Changes";
    *Oracle Solaris 11 Information Library*; Oracle and/or its affiliates;
    viewed 09 December 2025; available at:
    https://docs.oracle.com/cd/E23824_01/html/E24456/userenv-1.html
14. Debian; 2025; "UsrMerge - The Debian /usr Merge"; *Wiki*; Debian.org;
    viewed 09 December 2025; available at: https://wiki.debian.org/UsrMerge
15. Red Hat; 2025; "Changes/Unify bin and sbin"; *Wiki*; FedoraProject.org via
    Red Hat Inc. and others; viewed 09 December 2025; available at:
    https://fedoraproject.org/wiki/Changes/Unify_bin_and_sbin
16. Flatpak Team; 2025; "Introduction to Flatpak"; *Documentations*; Flatpak
    Team via @pradyunsg's Furo; viewed 09 December 2025; available at:
    https://docs.flatpak.org/en/latest/introduction.html
17. Red Hat; 2025; "Chapter 2. File System Structure and Maintenance";
    *Red Hat Enterprise Linux > 7 > Storage Administration Guide*; viewed
    09 December 2025; available at:
    https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-filesystem
18. The Linux Userspace API Group; 2025; "UAPI.9 Linux File System Hierarchy#";
    *UAPI Group Specifications*; Version 0.1; The Linux Userspace API Group;
    viewed 09 December 2025; available at:
    https://uapi-group.org/specifications/specs/linux_file_system_hierarchy/
19. FreeBSD; 2025; "`hier` - Miscellaneous Information Manual";
    *FreeBSD Manual Pages*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?hier(7)
20. FreeBSD; 2025; "Ports - Miscellaneous Information Manual";
    *FreeBSD Manual Pages*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?query=ports&sektion=7&apropos=0&manpath=FreeBSD+15.0-RELEASE+and+Ports
21. FreeBSD; 2025; "Chapter 4. Installing Applications: Packages and Ports";
    *FreeBSD Handbook*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://docs.freebsd.org/en/books/handbook/ports/
22. FreeBSD; 2025; "FreeBSD Porter's Handbook"; *FreeBSD Handbook*;
    The FreeBSD Project via The FreeBSD Community and The FreeBSD Foundation;
    viewed 09 December 2025; available at:
    https://docs.freebsd.org/en/books/porters-handbook/book/
23. FreeBSD; 2025; "`yp` - System Manager's Manual"; *FreeBSD Manual Pages*;
    The FreeBSD Project via The FreeBSD Community and The FreeBSD Foundation;
    viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?query=yp&manpath=FreeBSD+13.2-STABLE
24. FreeBSD; 2025; "`named` - Internet domain name server";
    *FreeBSD Manual Pages*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?query=named&sektion=8&manpath=OpenBSD+5.1
25. APPLE; 2017; "Bundle Structures"; *Documentation Archive - Bundle
    Programming Guide*; Apple Developer; Apple Inc.; Cupertino, California,
    USA; Viewed on 2026-04-30; Available at:
    https://developer.apple.com/library/archive/documentation/CoreFoundation/Conceptual/CFBundles/BundleTypes/BundleTypes.html#//apple_ref/doc/uid/10000123i-CH101-SW1
26. APPLE; 2018; "File System Basics"; *Documentation Archive - Bundle
    Programming Guide*; Apple Developer; Apple Inc.; Cupertino, California,
    USA; Viewed on 2026-04-30; Available at:
    https://developer.apple.com/library/archive/documentation/FileManagement/Conceptual/FileSystemProgrammingGuide/FileSystemOverview/FileSystemOverview.html




## Verifying Content Integrity

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

To secure the content from unauthorized modification by anyone down to bit-level
(`0|1`), they are cryptographically signed using one or more cryptography tools
such as but not limited to:

* [GnuPG](https://gnupg.org); AND/OR
* [OpenSSL](https://www.openssl.org/).

The public key and the associated certificate are attached. Only the main owner
keeps and maintains the private keys. To verify the content's integrity:



### GnuPG

1. Install [GnuPG](https://gnupg.org) software if not present.
2. Download the target file and its detached signature file (the `.asc` file
   with the same filename).
3. Download the public key file (`.gpg`).
4. Place them next to each other in the directory.
5. Open a terminal and execute the following command:

```
$ gpg --no-default-keyring --keyring /path/to/public.gpg --verify /path/to/file.asc
```



### OpenSSL

1. Install [OpenSSL](https://www.openssl.org) software if not present.
2. Download the target file and its detached signature file (the `.sig`/`.sign`
   file with the same filename).
3. Download the public certificate file (`.pem`) containing the public key
   within.
4. Place them next to each other in the directory.
5. Open a terminal and execute the following command:

```
$ openssl dgst -verify /path/to/pubkey.pem -signature /path/to/file.sig /path/to/file
```




## Artificial Intelligence (A.I.) Decrees

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Please refer to [AI_DECREES.md](AI_DECREES.md) for the project's policy on the
use of Artificial Intelligence.




## Maintainers' Notes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

1. Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for contributing &
   maintenances guidelines.




## License

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

* [Agreed GIMP License](.internals/terms-of-services/GimpORG-License.pdf)
* [Agreed GIMP Privacy Policy](.internals/privacy-policy/GimpORG-Privacy-Policy.pdf)
* [Agreed Inkscape License](.internals/terms-of-services/Inkscape-License.pdf)
* [Agreed Inkscape Privacy Policy](.internals/privacy-policy/Inkscape-Privacy-Policy.pdf)
* [Agreed LibreOffice License](.internals/terms-of-services/LibreOffice-License.pdf)
* [Agreed LibreOffice Privacy Policy](.internals/privacy-policy/LibreOffice-Privacy-Policy.pdf)

This entire repository is licensed under
[Creative Commons Attribution-NoDerivatives 4.0 International License](LICENSE.txt).
To ensure better understanding of this license, the following sub-sections will
briefly describe how to deploy the content.

For registered non-profit organizations (NGO), you are considered a
`Commercial Entity` the same as any for-profit organization by default. However,
you will be eligible for the NGO disbursement grant and receive exception
privileges from the creator(s).



### Attribution

Unless otherwise specified in writing, you **MUST** attribute back to the
creator(s) as follows:

```
Title: The Filesystem Hierarchy Layouts
Creators: (Holloway) Chew, Kean Ho
Packaged-By: (Holloway) Chew, Kean Ho
Contact: hello@chewkeanho.com
SKU: chewkeanho-research-the-filesystem-hierarchy-layouts
UUID: 3113F0A2-61BD-449C-BC0F-DE4C09997AC6
DOI: 10.5281/zenodo.17864564
License: Creative Commons Attribution-NoDerivatives 4.0 International License (https://creativecommons.org/licenses/by-nd/4.0)
Repository Made On: 2025-11-30
Repository Made From: Malaysia, South East Asia
Procure: https://doi.org/10.5281/zenodo.17864564
```



### Ownership - Personal

> [!NOTE]
>
> This targets any customer wanting to own a copy of the content and then only
> he/she is using it without sharing with any 3rd-party entity; AND **WITHOUT**
> any monetary intention such as but not limited to:
>
> * Saving a local copy and then viewing via his/her own mobile device(s); OR
> * Saving a local copy and then viewing via his/her own personal computer; OR
> * Saving a local copy for artificial intelligence data training purposes.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.



### Ownership - Commercial

> [!NOTE]
>
> This targets any customer wanting to own a copy of the content and then only
> he/she is using it without sharing with any 3rd-party entity; AND **WITH** any
> monetary intention such as but not limited to:
>
> * Saving a local copy for enhancing his/her company's procurement list; OR
> * Saving a local copy for commercial artificial intelligence data training
>   purposes.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.



### Reference - Personal & Commercial

> [!NOTE]
>
> This targets any customer wanting to refer or to provide a guide for sourcing
> the original content for any 3rd-party entity **without directly displaying
> any portion of the original content**; **WITHOUT** any monetary intention such
> as but not limited to:
>
> * Academic research and paper writing; OR
> * New content creation linking to the original content **WITHOUT displaying
>   any of the original content** for his/her own streaming platform; OR
> * Content production and collection linking to original content **WITHOUT
>   displaying any of the original content**; OR
> * Web portfolio project linking to the original content **WITHOUT displaying
>   any of the original content**; OR
> * Event materials linking the original content **WITHOUT displaying any of the
>   original content**; OR
> * Meeting materials linking the original content **WITHOUT displaying any of
>   the original content**; OR
> * Advertisement contents linking the original content **WITHOUT displaying any
>   of the original content**.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.



### Integration - Personal

> [!NOTE]
>
> This targets any customer wanting to directly **display portions and NOT ALL**
> of the original content **as it is OR without any composing remixes or
> modifications retaining the original intent, art direction and messages** into
> his/her content creation; **WITHOUT** any monetary intention such as but not
> limited to:
>
> * New content creation with displaying portion(s) of the original content for
>   his/her own streaming platform **without any monetary gain**; OR
> * Content production and collection with displaying portion(s) of the original
>   content **without any monetary gain**; OR
> * Web portfolio project with displaying portion(s) of the original content
>   **without any monetary gain**; OR
> * Event materials with displaying portion(s) of the original content
>   **without any monetary gain**; OR
> * Meeting materials with displaying portion(s) of the original content
>   **without any monetary gain**.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.



### Integration - Commercial

> [!NOTE]
>
> This targets any customer wanting to directly **display portions and NOT ALL**
> of the original content **as it is OR without any composing remixes or
> modifications retaining the original intent, art direction and messages** into
> his/her content creation; **WITH** any monetary intention such as but not
> limited to:
>
> * New content creation with displaying portion(s) of the original content for
>   his/her own streaming platform; OR
> * Content production and collection with displaying portion(s) of the original
>   content; OR
> * Web portfolio project with displaying portion(s) of the original content; OR
> * Event materials with displaying portion(s) of the original content; OR
> * Meeting materials with displaying portion(s) of the original content; OR
> * Advertisement materials with displaying portion(s) of the original content.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.



### Composition Remix - Personal

> [!NOTE]
>
> This targets any customer wanting to own and then **modify the original
> content extensively preserving or altering the original intent, art direction,
> or message** for composing his/her new content creation; **WITHOUT** any
> monetary intention such as but not limited to:
>
> * New content creation with digitally modified and processed original content
>   integration for his/her own streaming platform **WITHOUT** any profits
>   including advertisement commission; OR
> * Personal content production and collection with digitally modified and
>   processed original content integration for his/her own streaming platform
>   **WITHOUT** any profits including advertisement commission; OR
> * Personal web portfolio project with digitally modified and processed
>   original content integration for his/her own streaming platform **WITHOUT**
>   any profits including advertisement commission; OR
> * Social media meme content creation with digitally modified and processed
>   original content integration for his/her own streaming platform **WITHOUT**
>   any profits including advertisement commission.

You are **NOT ALLOWED** due to the license restriction.



### Composition Remix - Commercial

> [!NOTE]
>
> This targets any customer wanting to own and then **modify the original
> content extensively preserving or altering the original intent, art direction,
> or message** for composing his/her new content creation; **WITH** any monetary
> intention such as but not limited to:
>
> * New content creation with digitally modified and processed original content
>   integration for his/her own streaming platform; OR
> * Personal content production and collection with digitally modified and
>   processed original content integration for his/her own streaming platform;
>   OR
> * Personal web portfolio project with digitally modified and processed
>   original content integration for his/her own streaming platform; OR
> * Social media meme content creation with digitally modified and processed
>   original content integration for his/her own streaming platform.

You are **NOT ALLOWED** due to the license restriction.



### Broadcast or Resell Redistribution - Personal

> [!NOTE]
>
> This targets any customer wanting to share, to broadcast, to re-distribute,
> to sell, or to re-sell the original, **modified, OR derived** content
> **WITHOUT** any monetary intention such as but not limited to:
>
> * Sharing with family members; OR
> * Streaming the content via any streaming platform with private viewer
>   access; OR
> * Displaying the content in his/her gallery with privately invited guests; OR
> * Displaying the content in private, free entry open spaces like living room;
>   OR
> * Owning a copy of the original content and serving it as downloadable content
>   on a website in a private network (e.g. self-hosted home network); OR
> * Sharing the original content across social media or messaging applications
>   like email or instant messenger.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.



### Broadcast or Resell Redistribution - Commercial

> [!NOTE]
>
> This targets any customer wanting to share, to broadcast, to re-distribute,
> to sell, or to re-sell the original, **modified, OR derived** content
> **WITH** any monetary intention such as but not limited to:
>
> * Streaming the content via any streaming platform with public or private
>   viewer access; OR
> * Displaying the content in any company's public events with free or payable
>   guest invites; OR
> * Displaying the content in any company's internal/private events with free or
>   payable guest invites; OR
> * Owning a copy of the original content and serving it as free OR payable
>   downloadable content on his/her website in any network (Internet, Intranet,
>   or private networks); OR
> * Sharing the original content across social media or messaging applications
>   like email or instant messenger; OR
> * Distributing the original content via multiple profit-earning streaming
>   platforms.

You are **ALLOWED** provided that you **STRICTLY COMPLY** with the license
attribution.
