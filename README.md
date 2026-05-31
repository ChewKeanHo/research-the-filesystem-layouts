# The Filesystem Layouts | (Holloway) Chew, Kean Ho's Knowledge Research

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Having trouble working with filesystem hierarchy layouts especially those that
has standardized regulations like UNIX and Windows? Are you looking for some
design references that are comforming and portable to as many operating as
possible? This is the right research dataset.

At (Holloway) Chew, Kean Ho's The Filesystem Layouts Research Project, tech
volunteers and me are continuously updating this repository for abstracting
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
It is **100% human-made and direct artificial intelligences (A.I) contributions
(e.g. vibe coding) IS STRICTLY PROHIBITED**. Only A.I. usage is for
non-concequential tasks like scouting for data source materials across the
broken search engines and language corrections (e.g. grammar).

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
https://github.com/ChewKeanHo/research-the-filesystem-layouts). There
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

* **Architectures** - the general [_Architectures](/_Architectures) patterns.
* **FreeBSD** - the [_FreeBSD](/_FreeBSD) UNIX-like OS.
* **Linux** - the [_Linux](/_Linux)-based UNIX-like OS.
* **Microsoft Windows** - the [_Windows](/_Windows) Windows OS.

> [!IMPORTANT]
>
> For Linux, it is the consolidated version of all its distributions including
> but not limited to SystemD, FreeDesktop.org, Red Hat, Debian, Devuan,
> Void Linux, Fedora, etc.




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



## Design Sources & References

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

1. Please refer to [REFERENCES.md](REFERENCES.md) for source and references
   list.




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
Title: The Filesystem Layouts
Creators: (Holloway) Chew, Kean Ho
Packaged-By: (Holloway) Chew, Kean Ho
Contact: hello@chewkeanho.com
SKU: chewkeanho-research-the-filesystem-layouts
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
