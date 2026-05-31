# Views

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `View` holds the responsibilities for:

* Facilitates input|output rendering user interfaces using observer and bind
  them with the corresponding `ViewModels` functions.
* Enables|disables signal triggers of an input|output user interface.
* Response and re-render output interfaces based on new data from one or more
  `ViewModels` data processing.
* Calls backend private software for rendering processing.
* Managing only a single-type of response rendering.

A `View` can also be fully supplied by 3rd-party as a library module or a
wrapper to such when interfacing with package manager of a programming language.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing a `View`:

* **Handles business logics** - that is `ViewModels` layer's role.
* **Handles data processing logics** - that is `Models` layer's role.
* **Called by `Models`** - avoid that. That is `ViewModels` layer's role.
* **Called by `ViewModels`** - avoid that. `Views` is the one calling
  `ViewModels`; not the other way round. Resolve the data flow error.
* **Fusing either composite or compound approach with other `Views`** - avoid
  this at all cost to prevent complicated and unwanted spaghetti codes technical
  debt. Deploy a new `Views` if there is really a need and leave the original
  `Views` as it is unmodified.
* **Not implementing a reactive signal processing framework** - `MVVM` strictly
  relies on a reactive|signal|interrupt processing paradigm. Otherwise, it is
  a waste of time but use `MVC` architecture instead.
