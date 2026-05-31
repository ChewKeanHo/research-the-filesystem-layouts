#  ViewModels

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A `ViewModel` holds the responsibilities for:

* coordinate input data sanitization offered from `Models` layer.
* coordinate and control data processing business logic algorithms using
  `Models` layer.
* respond back to `Views` layer with the output data.




## Common Mistakes

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Among the common mistakes when implementing a `ViewModel`:

* **Pre-processing data before passing to `Models`** - that is `Models` layer's
  role. However, if the `Models` do not fulfill the requirement and there is no
  way to update them, create an interim `Model` wrapping the compromised one
  and have `ViewModels` call that instead.
* **Handling business logics algorithm** - that's **STRICTLY** a `View`'s role.
* **Fat `ViewModel`** - move it out into `Models` layer. `ViewModels` are thin
  and only coordinates `Models` layers by calling them.
