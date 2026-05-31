#  `Model-View-Controller` or `Model-View-Presenter`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the basic project model designed by Trygve Reenskaug back in late 1970s
while working on Smalltalk-79 as a visiting scientist at the
Xerox Palo Alto Research Center (PARC). It is very useful for small,
single-purpose programs and applications deployment. This is especially useful
architecture when complying with UNIX single well-done purpose design principle.

This design is sometimes known as `MVC` or `MVP` with the only difference of
`Controller` and `Presenter`. Such difference is mainly about grammar and
political jargons where one argues:

1. `Controller` hands over the control flow to the `model` and the `model` deals
   with the response completely; AND
2. `Presenter` handles the control flow entirely and both `model` and `views`
   are libraries to it.

One must know the difference since human resources (HR) and sometimes hiring
manager sometimes made these jargons up and claimed them as the common
industrial practices. Therefore, play well with them.




## Architecture Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

There are 3 main components:

* **models** - holds the data models with `create`, `read`, `update`, and
  `delete` interfaces for `controller`/`presenter` to call with.
* **views**  - holds the output interface design rendering with `read` and
  `update` interfaces for `controller`/`presenter` to call.
* **controller/presenter** - holds the coordination interfaces for the client
  side to call in. It calls `models` for data processing and `views` for
  response constructions.




## Data and Control Flows

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Jargons aside, `MVC`/`MVP` operates based on the following flow from client to
server per transaction:

1. `Client` calls the application's `main`/Server function/application
   programmable interface (API).
2. `main`/API function initializes and seek out the corresponding
   `controller`/`presenter` function.
3. `controller`/`presenter` function parse the inputs and call the correct
   `model` functions and process the data.
4. Depending on jargons:
   * If the `controller` is used:
     1. The `model` then calls the `view` function to construct the response.
     2. The `model` pass the response body back to the `controller`.
     3. The `controller` then return verbatim back to the client as output.
   * If the `presenter` is used:
     1. The `presenter` then calls the `view` function to construct the
        response body.
     2. The `presenter` returns the response body back to the client as output.
5. Transaction ends and `main`/API function is terminated with success.

A data flow diagram is shown as follows:

```
                              +---> Models
Client  <---> Presenter <-----+
 |  |                         +---> Views
 |  |
 |  |
 |  |
 |  |
 |  +-------> Controller ----> Models ----> Views ---+
 |                                                   |
 +-----<----------<----------<----------<------------+
```

> [!NOTE]
>
> Generally for any programming language, *the `Presenter` is the correct
> representation as each function must `return` at some point programmatically*.
>
> The `Controller` version is somewhat convincing but its cannot be represented
> programatically. If a `Controller` `return` the moment it passes the control
> to the `Models`, the entire transaction is ended pre-maturely. This
> representation only makes sense for any inexperienced programmer who happened
> to be a hiring manager. Play it well.




## Caveats

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

While `MVC`/`MVP` is simple to understand and theoretically is simple enough to
deploy, it **ONLY WORKS WELL** for grandular models and simple projects. This is
especially true back in 1970s all the way to 2000s when CPU processing power are
within MHz speed at maximum.


### Advanced Compounding/Compositing Data Models Complications

As of year 2026, data models today are often heavily integrated with one another
through either composite or compound relations (e.g. a `User` can have
multi-layers identity and authentications management data model (IAM) and a
separate personal identifiable information (PII) data model). `MVC`/`MVP` cannot
easily honor such separation of concerns and due to resources constriants, the
`model` often get spegetti-ed up making the entire project difficult to
maintain.


### Supply Chain Vulnerability

As of year 2026, `MVC`/`MVP` model is highly vulnerable to supply chain
vulnerability especially in composited or compounded data `model`s. Due to the
simplicity of its architecture patterns, 3rd-party libraries are often directly
integrated into `controller`/`presenter`.

Now, when the 3rd-party libraries' owner perform an *"After-the-Fact"* (or in
layman terms: *"rug pull"*) move (including bogus copyright infrigment lawsuit),
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

If there is any unresolvable caveat:

* `VIPER` architecture is a much better choice for both
  *frontend and backend implementation*.
* `MVVM` architecture is a much better choice for *frontend implementation*.

Successful deployments are:

1. UNIX "Do One Thing Only and Good" philosophy OS functionalities extensions.
2. Small and cleanly separated data models network server.
