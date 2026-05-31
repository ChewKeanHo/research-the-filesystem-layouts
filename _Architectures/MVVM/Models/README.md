#  Models

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `Model` holds the responsibilities for:

* Provisioning data sanitization functions for `ViewModels` to call.
* Provisioning data processing functions for `ViewModels` to call.
* Calls backend private software for data processing.
* Managing only a single-type of resources data.

A `Model` can also be fully supplied by 3rd-party as a library module or a
wrapper to such when interfacing with package manager of a programming language.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing a `Model`:

* **Handles business logics** - that is `ViewModels` layer's role.
* **Handles response rendering logics** - that is `Views` layer's role.
* **Called by `Views`** - avoid that. That is `ViewModels` layer's role.
* **Fusing either composite or compound approach with other `Models`** - avoid
  this at all cost to prevent complicated and unwanted spaghetti codes technical
  debt. Deploy a new `Model` if there is really a need and leave the original
  `Models` as it is unmodified.
