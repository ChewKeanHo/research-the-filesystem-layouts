#  `Model-View-ViewModel`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This architecture pattern is designed by Microsoft presented in
Windows Presentation Foundation (WPF). The idea is to use signal processing
via client's action reactivity to trigger a data processing. As such, this
pattern is ideal and heavily used for Graphical User Interface (GUI)-based
application.

The strong advantage of `MVVM` is a highly responsive application since
everything is based on user reactiveness. In theory, when user is not providing
any input, nothing is executed except the input observers.

This design is commonly known as `MVVM`.




## Architecture Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

There are 3 main components:

* **Models** - holds the data models with `create`, `read`, `update`, and
  `delete` interfaces for `view-models` to call.
* **Views** - holds the input and output interfaces rendering with `read` and
  `update` interfaces.
* **ViewModels** - holds the data processing functions with `create`, `read`,
  `update`, and `delete` interfaces for `views` to call.




## Data and Control Flows

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

1. `Client` calls the application's `main`/Server function/application
   programmable interface (API).
2. `main`/API function initializes and seeks the corresponding `Views` function.
3. `Views` function received `Client`'s signal and calls its corresponding
   binded `ViewModels` reactive function.
4. `ViewModels` calls the `Models` function for data processing with new data as
   response body.
5. `ViewModels` returns the response body back to `Views` function.
6. `Views` function received the new data and update the rendering layout.
7. Transaction ends and `main`/API function is terminated with success.

A data flow diagram is shown as follows:

```
Client  <---> Views <---> ViewModels <---> Models
```




## Caveats

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Unlike `MVC`, `MVVM` has a list of its own caveats on top of `MVC` ones.


### Compulsory Understanding of Reactive/Signal/Interrupt Processing

Unlike `MVC` and `VIPER`, `MVVM` depends heavily on reactive/signal (or from
hardware folks: interrupt) processing paradigm. Since the entire idea is based
on how the Client reacts on the GUI from `Views` layer (e.g. pressing a button).

Among other vital knowledge are signal processing like filtering spams, wait
and observe, process pipelining, concurrent processing, parallel processing,
transactional atomization, etc. Generally, this entire signal processing
construct itself is a framework of its own.

Therefore, this paradigm can unconventional for inexperienced developers.


### Possible Resources Intensive Weakness

As the control is passed into `Views` layer and every single input rendering is
an observer server, GUI design with many inputs can cause significant computer
resources consumption on stand-by.

Hence, each `Views` presentation **MUST** have well designed user-experience
with limited inputs at a time for optimized resources vs. performance
throughput.


### Advanced Compounding/Compositing Data Models Complications

As of year 2026, data models today are often heavily integrated with one another
through either composite or compound relations (e.g. a `User` can have
multi-layers identity and authentications management data model (IAM) and a
separate personal identifiable information (PII) data model). `MVVM` cannot
easily honor such separation of concerns and due to resources constriants, the
`Model` often get spegetti-ed up making the entire project difficult to
maintain.


### Supply Chain Vulnerability

As of year 2026, `MVVM` architecture is highly vulnerable to supply chain
vulnerability especially in composited or compounded data `Models`. 3rd-party
libraries are often directly integrated into all layers instead.

Now, when the 3rd-party libraries' owner perform an "After-the-Fact" (or in
layman terms: "rug pull") move (including bogus copyright infrigment lawsuit),
it is highly difficult to untangle these libraries.


### Unable to Cope Chaotic Changes

When chaotic changes are introduced from all sides like:

1. Designer team only need to deal with responses' viewing layout changes; AND
2. Security audit team only needs to deal with penetration testing; AND
3. Data development team only needs to deal with library development; AND
4. Business and user experience developer can enable/disable application
   features from time to time; AND
5. Tester can test independent layers whenever resources permits OR a quick and
   holistic coverage when resources are scarce.

It is very clear that all chaos sources are bottlenecked to the application
developer itself. Hence, it becomes a process congestion and a deep technical
debt when the application scales up.




## When to Deploy

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The main constraint is to ensure all the caveats are mitigated before any
design decisions.

If the application is a client-side only GUI application (also known as pure
frontend), `MVVM` is generally the ideal architecture due to its high
responsiveness despite its caveats. Most of all, if the client-side only GUI
application does not process data on its own, some of the caveats are no longer
applicable.

Otherwise, for server-side processing or having any unresolvable caveat,
*`VIPER` architecture pattern is a much better choice*.

Successful deployments are:

1. Amost all iOS applications (GUI).
2. Amost all Android applications (GUI).
2. Amost all Web App applications (GUI).
