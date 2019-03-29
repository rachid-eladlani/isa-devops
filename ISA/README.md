# Introduction to Software Architecture (2018-19)

## Teaching Staff

  * [Philippe Collet](collet@i3s.unice.fr), Université Côte d'Azur, CNRS, I3S (co-head, ISA)
  * [Anne-Marie Pinna-Déry](pinna@unice.fr), Université Côte d'Azur, CNRS, I3S
  * [Laureen Ginier](laureen.ginier@univ-cotedazur.fr), IBM France Lab, Université Côte d'Azur


## Lecture Material

  - Lecture #1: Introduction to ISA
    - [#1.1: Introduction](https://github.com/collet/isa-devops/blob/master/ISA/week1_isa_intro_v0.1c.pdf)
    - [#1.2: N-tiers Architectures](https://github.com/collet/isa-devops/blob/master/ISA/week1_isa_archi_n_tiers.pdf)
  - Lecture #2: JavaEE, EJB 101 (Dependency Injection, Session and Entity), ORM 101
    - [#2: EJB 101](https://github.com/collet/isa-devops/blob/master/ISA/week2-javaEE-ejb-orm-v02.pdf)
  - Lecture #3: Architectural viewpoints
    - [#3.1: Architectural viewpoints - introduction](https://github.com/collet/isa-devops/blob/master/ISA/ViewpointsV2Intro-1.pdf)
    - [#3.2: Architectural viewpoints - concepts](https://github.com/collet/isa-devops/blob/master/ISA/Viewpoints%20V2-1.pdf)
  - Lecture #4: From Client/Server to Web Services
    - [#4.1: Background on Protocols, Client/Serve, RMI and RPCs (french)](https://github.com/collet/isa-devops/blob/master/ISA/CS-RMI-RPC-Protocoles.pdf)
    - [#4.2: Services and interoperability (french and english)](https://github.com/collet/isa-devops/blob/master/ISA/servicesEtInterope%CC%81rabilite%CC%8113mars.pdf)
    - [#5: Persistence, JPA, and related tricks](https://github.com/collet/isa-devops/blob/master/ISA/week5-persistence-v02.pdf)

### Examples of _good_ architecture reports (FR):

  - 2015: The Cookie Factory. [Report #1](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2015_1.pdf), [Report #2](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2015_2.pdf)
  - 2016: Isola 3000. [Report #1](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2016_1.pdf), [Report #2](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2016_2.pdf)
  - 2017: Disloyalty card. [Report #1](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2017_1.pdf) [Report #2](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2017_2.pdf)

### Previous exams (FR)

  - [2017](https://github.com/collet/isa-devops/blob/master/ISA/exams/exam_2017.pdf)
  - [2018](https://github.com/collet/isa-devops/blob/master/ISA/exams/exam_2018.pdf)

## Deliverables

### Architecture Report

You must deliver a PDF file at the root of your `main` repository on Github, named `architecture.pdf`. There is no page limits but _concision_ is an evaluation criteria (and your report should be ~10 pages long): *Monday 25th, February, 8:00pm*

It must contain the following architecture description:

  - Use cases diagrams;
  - Business objects definition as class diagram;
  - Interfaces pseudo-code definition (_e.g._, Java like);
  - Components described by a component diagram;

Each artefact must be justified with respect to its relevance in your architecture.

Non-exhaustive list of common pitfalls to avoid in your work:

  - spending (way) too much time on use cases definition and description;
  - defining interfaces and components that do not support than _business_;
  - Weird responsibilities for components (_e.g._, god component, disconnected assemblies, dangling element)
  - Lack of proper description/justification for the interfaces
  - Interfaces that relies on _ids_ and primitive objects (_e.g._, String, Integers) instead of business objects.


### Final Project Delivery

  - you need to deliver according to the instructions (TBD)
  - at the root, you should have a `components.pdf` file representing your component diagram
  - at the root, you should have a `archi.md` file representing your architecture report
  - the deliverable for both ISA and DevOps will be extracting using a specific script (soon available). Make sure your git repository tag is correct.
