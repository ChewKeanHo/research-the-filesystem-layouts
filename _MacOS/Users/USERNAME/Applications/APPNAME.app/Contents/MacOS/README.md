# `/Users/[USERNAME]/Applications/[APPNAME].app/Contents/MacOS`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses the app's executables. It can be many executables
(e.g., command line operator, server operator) but it **MUST** have one main
executable.

The main executable **MUST**:

1. Have **THE SAME** name as the `[APPNAME]` but without the `.app`; AND
2. Statically compiled by XCode.

This directory is the same as UNIX-based OSes' `bin/` directory.
