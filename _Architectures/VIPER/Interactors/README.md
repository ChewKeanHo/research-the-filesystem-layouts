#  Interactors

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

An `Interactor` holds the following responsibilities:

* Developing business logic functions using `Entities` layer and `Views` layer
  for `Presenters` layer to call upon.
* Isolating any chaotic changes introduced by 3rd-parties libraries' owners from
  damaging the business logics layers (`Interactors`, `Presenters`, and
  `Routers`).
* Coordinate input data sanitization offered from `Entities` layer.
* Coordinate and control data processing business logic algorithms using
  `Entities` layer.
* Coordinate and control response body constructions and rendering with `Views`
  layer.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing an `Interactor`:

* **Pre-processing data before passing to `Entities`** - that is `Entities`
  layer's role. However, if the `Entities` does not fulfill the requirement and
  there is no way to update them, this is allowed as interim solution.
* **Handling business logics algorithm** - that's **STRICTLY** a `Presenter`'s
  role.
* **Fat `Interactor`** - move it out into `Entities` layer. `Interactors` are
  thin and only coordinates `Entities` and `Views` layers by calling them.
