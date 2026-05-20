# `[FRAMEWORKNAME].framework/Versions`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all versions of the framework's resource files. Older
versions are facilitated for backward compatibilities and de-couple the
framework's development progress away from any external projects.

The `Current/` directory version is actually a symbolic link pointing to a
specific version (e.g. `v1.0.0`) with relative path (`Versions/Current` ->
`Versions/v1.0.0`). The framework developer only needs to update the
`Versions/Current` symbolic link pointer from time to time for rolling out new
releases.

It is **HIGHLY RECOMMENDED to import the specific version** rather than
importing the `Current` latest ones. This de-couples the project development
away from the supplied framework's own development progress (e.g. breaking
changes release cycles).

If you are developing using XCode, then you may structure your content
accordingly.

Since `iOS` is **DISALLOWED AND PROHIBITED** to create a framework bundle in
production, there is nothing to worry about beyond XCode development usage.
