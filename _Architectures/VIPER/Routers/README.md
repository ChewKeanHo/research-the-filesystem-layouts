#  Routers

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `Router` holds the following responsibilities:

* Coordinates application's actions and call the corresponding `Presenter`
  function.
* Optionally facilitates input|output rendering user interfaces using observer
  and bind them with the corresponding `Presenter` functions when
  reactive|signal|interrupt processing paradigm.
* Optionally enable|disable signal triggers of an input|output user interface.
* Response and re-render output interfaces based on new data from one or more
  `Presenter` data processing.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing an `Interactor`:

* **Calling `Entities`, `Views`, and `Interactors`** - avoid that. Have them set
  in a `Presenter` function and then call the `Presenter` function instead.
  Maintain the isolation.
* **Calling multiple `Presenters`** - It is an error. `Routers` call only 1
  `Presenter` per route. Fix the error.
* **Handles any data processing** - avoid that. Send them to an `Interactor`
  function, have it called by the `Presenter` function; and then call it
  instead. `Routers` are **STRICTLY** mapping the `Presenter` functions only.
