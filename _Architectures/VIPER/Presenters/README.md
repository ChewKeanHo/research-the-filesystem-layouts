#  Presenters

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `Presenter` holds the following responsibilities:

* Coordinates business logic functions using `Interactors` layer.
* Responds to the client request from `Routers` layer.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing an `Interactor`:

* **Calling `Entities` or `Views`** - avoid that. Isolate them into their
  respective `Interactor` functions. Then call using the `Interactors` only.
  Maintain the isolation.
* **Calling `Routers`** - It is an error. `Routers` call `Presenters`; not the
  other way round. Fix the error.
* **Handles data processing before calling to any `Interactor`** - avoid that.
  Send them to an `Interactor` function and call it instead. `Presenters` are
  **STRICTLY** coordinations.
* **Fat `Presenters`** - move it out into `Interactors` layer and subsequently
  new `Entities` or `Views` layers. `Presenters` are **STRICTLY** coordinations.
