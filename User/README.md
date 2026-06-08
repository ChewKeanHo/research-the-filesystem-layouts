# User Home Directory Layout

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Now let us review the user home directory layout. This layout is used across
various operating systems and was abstracted from all major OSes including
`FreeBSD`, `Linux`‑based OSes (a consolidation of `SystemD`, `FreeDesktop.org`,
`Red Hat Linux`, `Debian`, `Devuan`, `Void Linux`, `Fedora`), Apple’s `MacOS`,
and Microsoft `Windows`.

For Microsoft `Windows`, due to its design and the absence of a formal
filesystem hierarchy standard, this layout focuses mainly on deployment rather
than modifying the operating system itself.

Each directory in the user home layout serves specific graphical user interface
(GUI) purposes and functionalities. Exploring each directory helps one better
understand the rationale behind its structural design.

This layout captures only the directories that appear natively in any of the
surveyed operating systems.

Users should be allowed to perform manual installation (e.g., copy‑pasting a
bundle into their home directory). Otherwise, they may become silently
rebellious and attempt to crack the operating system, which is an undesirable
outcome.

> [!WARNING]
>
> This is **NOT** a rule. Depending on the operating system, each user may
> customize his or her home directory at personal discretion. Some savvy users
> alter the structures with great creativity (e.g., combining `Videos`, `Music`,
> and `Pictures` into a single, well‑maintained `Galleries` directory).
