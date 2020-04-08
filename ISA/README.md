# Introduction to Software Architecture (2019-20)

## Teaching Staff

  * [Philippe Collet](collet@i3s.unice.fr), Université Côte d'Azur, CNRS, I3S (co-head, ISA)
  * [Anne-Marie Pinna-Déry](pinna@unice.fr), Université Côte d'Azur, CNRS, I3S
  * [Laureen Ginier](laureen.ginier@univ-cotedazur.fr), IBM France Lab, Université Côte d'Azur


## Lecture Material

  - Lecture #1: Introduction to ISA
    - [#1.1: Introduction] https://github.com/collet/isa-devops/blob/master/ISA/1_1_kickoff-1920.pdf
    - [#1.2: N-tiers Architectures] https://github.com/collet/isa-devops/blob/master/ISA/1_2_Archi_N_Tiers-1920.pdf
  - Lecture #2: JavaEE, EJB 101 (Dependency Injection, Session and Entity), ORM 101
    - [#2: EJB 101] https://github.com/collet/isa-devops/blob/master/ISA/2_javaEE-ejb-orm-1920.pdf
  - Lecture #3: C/S and Architectural viewpoints
    - [#3.1: Background on Protocols, Client/Serve, RMI and RPCs (french)] https://github.com/collet/isa-devops/blob/master/ISA/3_1_IntroR%C3%A9seauApplicatifRMI-RPC-Protocole.pdf
    - [#3.2: Architectural viewpoints] https://github.com/collet/isa-devops/blob/master/ISA/3_2_Viewpoints.pdf
  - Lecture #4: Web Services
    - [#4: Services and interoperability] https://github.com/collet/isa-devops/blob/master/ISA/4_servicesEtInteroperabilite-6mars.pdf
  - Lecture #5: Persistence
    - [#5.1 : Persistence and JPA] https://github.com/collet/isa-devops/blob/master/ISA/5_persistence-part1-1920.pdf (video: https://unspod.unice.fr/video/7141-persistance-1-introduction-to-software-architecture-polytech-nice-sophia-si4/ )
    - [#5.2 : Persistence chapter of the cookie factory] https://github.com/collet/4A_ISA_TheCookieFactory/blob/develop/chapters/Persistence.md
    - [#5.3 : Persistence tricks] https://github.com/collet/isa-devops/blob/master/ISA/5_persistence-part2-1920.pdf (video: https://unspod.unice.fr/video/7142-persistance-2-introduction-to-software-architecture-polytech-nice-sophia-si4/ )
  - Lecture #6: Stateful and stateless session beans
    - [#6.1: EJB Sessions] https://github.com/collet/isa-devops/blob/master/ISA/6_ejb_session.pdf
    - [#6.2: Session and persistence] https://github.com/collet/isa-devops/blob/master/ISA/6_add-SessionBeansEtPersistance.pdf
  - Lecture #7: Interceptors and MOM
    - [#7: Interceptors and MOM] https://github.com/collet/isa-devops/blob/master/ISA/7_j2e_plus_plus%202020%20.pdf

### Examples of _good_ architecture reports (FR):

  - 2015: The Cookie Factory. [Report #1](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2015_1.pdf), [Report #2](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2015_2.pdf)
  - 2016: Isola 3000. [Report #1](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2016_1.pdf), [Report #2](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2016_2.pdf)
  - 2017: Disloyalty card. [Report #1](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2017_1.pdf) [Report #2](https://github.com/collet/isa-devops/blob/master/ISA/reports_examples/2017_2.pdf)

### Previous exams (FR)

  - [2017](https://github.com/collet/isa-devops/blob/master/ISA/exams/exam_2017.pdf)
  - [2018](https://github.com/collet/isa-devops/blob/master/ISA/exams/exam_2018.pdf)
  
## Assignment #1

First Assignment requires you to compile and package the code base of The Cookie Factory. The code base is available [in this repository (develop branch)](https://github.com/collet/4A_ISA_TheCookieFactory).

## Assignment #2

Build an architecture report for the case study.

## Deliverables

### Architecture Report (first report)

You must deliver a PDF file at the root of your `main` repository on Github, named `architecture.pdf`. There is no page limits but _concision_ is an evaluation criteria (and your report should be ~10 pages long): *Monday 17th, February, 8:00pm*

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


### Final Project Delivery (deadline: TBD)

  - you need to deliver according to the instructions of the DevOps part +
  - at the root, you should have a `components.pdf` file representing your component diagram
  - at the root, you should have a `archi.md` file representing your architecture report:
      - Overview: a paragraph on what is provided (how many CLIs, coverage of the functionalities, etc.)
      - Components: additional explanations over the components organization as shown in `components.pdf`
      - Pros: Strong points of your architecture
      - Cons: Weak points of your architecture 
  - the deliverable for both ISA and DevOps will be extracting using a specific script. Make sure your git repository tag is correct (see DevOps part as well).
