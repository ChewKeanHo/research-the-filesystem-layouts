# `var/mail`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient email files. They are generally `.eml` based
(some may be custom).

Due to many mailer services exist and mailboxes are typically owned by a person,
careful directory organization is advised. Also, assume every logged‑in user is
an email hoarder; this directory can grow very large in a short time.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `mail`** as it represent the entire mail
directory.

The file extension can be anything and nothing.

It is a practice to house the files using `trademark` and `product` naming
convention pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/mail/
  trademark_product
  ...

OR

var/mail/
  product
  ...
```
