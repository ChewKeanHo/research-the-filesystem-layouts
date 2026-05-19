# `/Users/[USERNAME]/Pictures`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's images files. The initial design was to let the
user save all images in this directory. Expected files are `.png`, `.jpg`,
`.svg`, `.webp`, `.avif`, and etc.

Only admin-privileged (`wheel`) and owning users can access this directory.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.
