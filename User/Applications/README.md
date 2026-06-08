# `Applications`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all packaged application bundles installed by the owning
user without requiring administrator privileges (e.g. a user with `wheel`
privilege on UNIX-based OSes). It was first introduced by Apple’s macOS, where
user‑specific application bundles are placed here.

For security, an operating system may implement content cryptographic signing
and distributor notarization, similar to how the Apple Developer Program
operates.




## OS Deployment

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The following operating systems deploy this directory:

1. Apple's `MacOS`.
2. Microsoft `Windows` (It is called `AppData/Local/Programs` instead).
