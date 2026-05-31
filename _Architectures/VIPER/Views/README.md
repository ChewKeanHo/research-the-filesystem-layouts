# Views

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `View` holds the responsibilities for:

* Optionally provisioning response body rendering input sanitization functions
  for `Interactors` to call.
* Provisioning response body rendering functions for `Interactors` to call.
* Calls backend private software for rendering processing.
* Managing only a single-type of response rendering.

A `View` can also be fully supplied by 3rd-party as a library module or a
wrapper to such when interfacing with package manager of a programming language.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing a `View`:

* **Handles business logics** - that is `Interactors` layer's role.
* **Handles data processing logics** - that is `Entities` layer's role.
* **Called by `Entities`** - avoid that. That is `Interactors` layer's role.
* **Fusing either composite or compound approach with other `Views`** - avoid
  this at all cost to prevent complicated and unwanted spaghetti codes technical
  debt. Deploy a new `Views` if there is really a need and leave the original
  `Views` as it is unmodified.
