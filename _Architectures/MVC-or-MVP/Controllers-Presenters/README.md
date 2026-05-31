#  Controllers|Presenters

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `Controller`|`Presenter` holds the responsibilities for:

* Identifying an application programmable interface (API) endpoint.
* Coordinate input data sanitization offered from `Models` layer.
* Coordinate and control data processing business logic algorithms using
  `Models` layer.
* Coordinate and control response body constructions and rendering with `Views`
  layer.
* Respond back to Client with the rendered response body.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing a `Controler`|`Presenter`:

* **Pre-processing data before passing to `Models`** - that is `Models` layer's
  role. However, if the `Models` do not fulfill the requirement and there is no
  way to update them, create an interim `Model` wrapping the compromised one
  and have `Controllers`|`Presenters` call that instead.
* **Fat `Controller`|`Presenter`** - move it out into `Models` layer.
  `Controllers`|`Presenters` are thin and only coordinates `Models` and `Views`
  layers by calling them.
