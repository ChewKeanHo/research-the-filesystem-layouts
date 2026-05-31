#  Entities

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

An `Entity` holds the responsibilities for:

* Provisioning data sanitization functions for `Interactors` to call.
* Provisioning data processing functions for `Interactors` to call.
* Calls backend private software for data processing.
* Managing only a single-type of resources data.

An `Entity` can also be fully supplied by 3rd-party as a library module or a
wrapper to such when interfacing with package manager of a programming language.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing a `Entity`:

* **Handles business logics** - that is `Interactors` layer's role. Focus on
  facilitating resources data management.
* **Fusing either composite or compound approach with other `Entities`** - avoid
  this at all cost. It is `Interactors` layer role to do such fusing. Leave the
  original `Entities` as it is unmodified.
* **Called by `Views`** - avoid this at all cost. It is `Interactors` layer role
  to do such fusing. Leave the original `Views` as it is unmodified.
* **Called by `Presenters`** - avoid that. Wrap it under an `Interactor`
  function and then have it called by the `Presenters`. Maintain the isolation
  among each other.
* **Called by `Routers`** - avoid that. Wrap it under an `Interactor` function,
  then called by a `Presenter`, which is called by the `Router`. Maintain the
  isolation among each other.
