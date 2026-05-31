#  `View-Interactor-Presenter-Entity-Router`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the advanced project model derived from the historical development and
learning from `Model-View-Controller` (`MVC`)/`Model-View-Presenter` (`MVP`) and
`Model-View-ViewModel (`MVVM`) architecture patterns. This developed by the
Apple iOS developers community to overcome the caveats. Since this is an
advancement from existing architectures, it requires a deeper learning and
hands-on experience to appreciate its architecture.

This design is commonly known as `VIPER` and was based on Clean Architecture by
Robert C. Martin (Uncle Bob).




## Architecture Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

There are 5 main components:

* **Models** - holds the data models with `create`, `read`, `update`, and
  `delete` interfaces for `interactors` to call.
* **Views** - holds the output interface design rendering with `read` and
  `update` interfaces for `interactors` to call.
* **Interactors** - holds the applications business libraries with `create`,
  `read`, `update`, and `delete` interfaces for `presenter` to call.
* **Presenters** - holds the business logics interfaces for the `routers` to
  call.
* **Routers** - holds the user experience coordination and business flows for
  client to call.




## Data and Control Flows

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The following flow from client to server per transaction:

1. `Client` calls the application's `main`/Server function/application
   programmable interface (API).
2. `main`/API function initializes and seek out the corresponding `Router`
   function.
3. `Router` function calls the corresponding `Presenter` business logic
   function.
4. `Presenter` function calls the underlying `Interactor` functions to process
   the data and query.
5. `Interactors` calls the respective `Entities` functions for data processing.
6. `Interactors` calls the respective `Views` functions for constructing the
   response body and returns back to `Presenter` function as output.
7. `Presenter` function returns the response body as output.
8. `Router` function returns the response body as output.
9. Transaction ends and `main`/API function is terminated with success.

A data flow diagram is shown as follows:

```
                                                          +---> Entities
Client <---> Router <---> Presenter <---> Interactors <---+
                                                          +---> Views
```




## Strength

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

As an upgrade to the `MVC`/`MVP` architecture, it definitely **MUST** counter
their caveats.


### Countering Composited and Compounded Libraries

Given that the `Interactors` layer is constructing the business functions,
the layer itself is facilitating the libraries fusing from either composite or
compound. This **DOES NOT** force the fusing directly into the 3rd-party
supplied or raw data libraries (`Entities` layer) like `MVC`/`MVP` does.


### Built-in Reactive Processing

Like `MVVM`, `VIPER` can handle reactive programming natively where `Routers`
layer handles all the signal processing. This enables `VIPER` to be deployed in
both frontend and backend without additional learning curve.


### Countering Supply Chain Vulnerability

Now that all the libraries are left in-tact inside `Entities` layer and the
business functions in `Interactors` layer, this clean separation isolates any
3rd-party introduced chaos only affecting the `Entities` layer.

Due to `Entities` layer not interacting with one another, it is **VERY EASY** to
deal with the 3rd-party libraries directly with high confidences not breaking
the entire business application.


### Facilitates Chaotic Changes From All Directions

Due to the `Routers`, `Presenters`, and `Interactors` separation layers, this
architecture facilitates maximum chaotic changes from any direction:

1. Designer team only need to deal with `Views` and `Interactors` layer.
2. Security audit team only needs to deal with `Routers` layer.
3. Data development team only needs to deal with `Models` and `Interactors`
   layer.
4. Business and user experience developer can enable/disable application
   features using `Routers` and `Presenters` layers.
5. Tester can test independent layers whenever resources permits OR directly
   on `Presenters` layer for a quick and holistic coverage when resources are
   scarce.

Now that VIPER can handle chaotic nature in a realiable manner, an application
can scale infinitely large without needing a migration.




## Caveats

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

`VIPER`, while having `MVC`|`MVP` and `MVVM` architectures' caveats resolved,
has its own caveats listed here.


### Higher Learning Curve

`VIPER` obviously has a higher learning curve compared to other architectures
especially when one does not have any development experience.


### Optional Understanding of Reactive/Signal/Interrupt Processing

When `VIPER` is deployed for reactive/signal (or from hardware folks: interrupt)
processing paradigm like Graphical User Interface (GUI) application, there is a
learning requirement for such processing paradigm.

Among other vital knowledge are signal processing like filtering spams, wait
and observe, process pipelining, concurrent processing, parallel processing,
transactional atomization, etc. Generally, this entire signal processing
construct itself is a framework of its own.

Therefore, this paradigm can unconventional for inexperienced developers.




## When to Deploy

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When the team has a strong documentation on how `VIPER` architecture pattern
works, `VIPER` architecture is always the preferred and default approach.

Successful deployments are:

1. large scale `iOS` and `MacOS` applications.
2. large scale web server applications.
