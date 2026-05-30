#  Patterned Directory Architectures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the patterned directory architectures covering common practices such
as but not limited to:

* **MVC** or **MVP** - model, view, controller/presenter structure; AND
* **MVVM** - model, view, view-model structure; AND
* **VIPER** - view, interactor, presenter, entity, and router structure.




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Usually, when a project is initialized, most of directory structuring are
chaotic and limitless. Overtime, the software industry developed some best
practices for quick adapation and single point of learning. The primary
objectives are:

1. enables people to easily and seamlessly collaborate with each other's
   projects without massive re-learning.
2. establishes a common understanding of data and control flows for a project.




## Forces of Chaos

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

A good architecture pattern is one that ideally can withstand any force of
chaos. For this project, we look into the following chao agents.


### Compounding/Compositing Data Models' Advancement Complications

As of year 2026, data models today are often heavily integrated with one another
through either composite or compound relations (e.g. a `User` can have
multi-layers identity and authentications management data model (IAM) and a
separate personal identifiable information (PII) data model).

An architecture **MUST** be able to facilitate such development without any
compromise or customizations to any of the data models libraries.


### Supply Chain Vulnerability

As of year 2026, supply chain vulnerability especially in composited or
compounded data `model`s is an important chaos factor to consider. When the
3rd-party libraries' owner perform an *"After-the-Fact"* (or in layman terms:
*"rug pull"*) move (including bogus copyright infrigment lawsuit).

An architecture **MUST** be able to cleanly facilitate a method to counter any
of the chaotic suppliers' shenanigans without any compromise.


### Chaotic Changes From Multiple Sources

In practice, a project usually encounters many chaos from multiple sources. For
this project, we consider:

1. Designer team only need to deal with responses' viewing layout changes; AND
2. Security audit team only needs to deal with penetration testing; AND
3. Data development team only needs to deal with library development; AND
4. Business and user experience developer can enable/disable application
   features from time to time; AND
5. Tester can test independent layers whenever resources permits OR a quick and
   holistic coverage when resources are scarce.

An architecture **MUST** be able to cleanly counter all the chaos agents without
any compromise.


### Reactive/Signal/Interrupt Processing

Modern user-oriented client-side application like Graphical User Interface (GUI)
app, there is a requirement to support reactive/signal (or from hardware folks:
interrupt) processing paradigm.

Among other vital knowledge are signal processing like filtering spams, wait
and observe, process pipelining, concurrent processing, parallel processing,
transactional atomization, etc. Generally, this entire signal processing
construct itself is a framework of its own.

Therefore, this paradigm can unconventional for inexperienced developers.

An architecture **MUST** be able to cleanly integrate this feature
**OPTIONALLY** without any compromise.


### Learning Curve

The cost of learning for inexperienced developer is considered based on both
complexity and speed.

An architecture **MUST** be able to seamlessly learnable in the fastest manner
in order to be deemed worthy of low learning curve.
