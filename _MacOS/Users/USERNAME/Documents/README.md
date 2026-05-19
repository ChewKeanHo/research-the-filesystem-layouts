# `/Users/[USERNAME]/Documents`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's data files. The initial design was to let the
user works exclusively in this directory. Expected files are documents,
databases, spreadsheets, etc.

Only admin-privileged (`wheel`) and owning users can access this directory.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.
