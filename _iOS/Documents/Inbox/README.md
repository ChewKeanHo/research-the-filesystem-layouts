# `Documents/Inbox`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all data readily to be opened by an outside entities.
Example:

1. User open an email attachment.
2. Mail program places email attachments associated with an app here.
3. That app silently move the file into appropriate location outside of this
   directory.
4. That app open the file and takes over hosting user experience (e.g., viewing,
   editing).

Apps are allowed to read and delete in this directory and **NOT** create or
write to existing files.

The contents are backed up by iTunes and iCloud.
