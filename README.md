# Introduction to Software Architecture & DevOps (2019-20)

## Rationale

In this course, we will address the same case study under two different but complementary point of views: _software architecture_ and _DevOps_. For the software architecture part, we will focus on the definition of an _n-tiers_ architecture using software components (implemented as EJBs using the J2E framework). A part of the architecture will also be developed in .Net, emphasising the need to support system interoperability using Web Services. For the DevOps part, we will address the difficult problem of aligning the _dev_ team with the _ops_ one to build a given piece of software. How to slice the code into independent modules that can be compiled, tested and deployed in a continuous way? How to properly test the integration between such loosely coupled components?

The course is scheduled each Friday, during semester #8. The course requires to be fluent in Java, and a strong background in object-oriented programming. The case study is the same for the whole course, and requires a strong investment in software development by teams of four students. Splitting your team into two sub-teams, one for the architecture part and one for the devops one is __definitively not a winning strategy__ (been there, done that).

The whole project relies on an open-source reference implementation of _The Cookie Factory_, a system to sell cookies to delighted customers, which will been made available to you within the Github classroom we'll be using for the exercices..

## Teaching Staff

  * [Philippe Collet](collet@i3s.unice.fr), Université Côte d'Azur, CNRS, I3S (co-head, ISA)
  * [Guilhem Molines](guilhem.molines@univ-cotedazur.fr), IBM France Lab, Université Côte d'Azur (co-head, DevOps)
  * [Anne-Marie Pinna-Déry](pinna@unice.fr), Université Côte d'Azur, CNRS, I3S (ISA)
  * [Laureen Ginier](laureen.ginier@univ-cotedazur.fr), IBM France Lab, Université Côte d'Azur (ISA)
  * [Salah Dahmoul](Salah.DAHMOUL@univ-cotedazur.fr), Orange, Université Côte d'Azur (DevOps)

### Specific pages (e.g., lectures material, deliverable contents)

  * [Introduction to Software Architecture](https://github.com/collet/isa-devops/tree/master/ISA/README.md)
  * [DevOps & Continuous Testing](https://github.com/collet/isa-devops/tree/master/DevOps/README.md)

### Case study description: 

  * [Drone Delivery](https://github.com/gmolines/isa-devops/blob/master/DroneDelivery.pdf)

## Planning 

![Planning](https://github.com/collet/isa-devops/blob/master/planning-covid.png)

  - Blue sessions are related to _ISA_
  - Green sessions are related to _DevOps_
  - Red sessions are related to _examinations_ (defence or written exam)

### Deliveries & Milestones

Deliveries are automatically extracted from the _github_ repository of the team. Details are given in the evaluation part of each part (ISA and DEVOPS). See below.

- Monday, February 17th, 8:00pm : first architecture report

### Evaluation

Even if the case study is shared and the course merged, this is administratively talking two different courses. As a consequence, the evaluation must be separated.

Evaluation is organized as follows:

  - _Introduction to Software Architecture_ : https://github.com/collet/isa-devops/blob/master/ISA/README.md
    - Architecture report: 15%
    - Intermediate demonstration (technical interview): 10%
    - Final demonstration (technical interview): 30%
    - Individual question (during tech interview): 15%
    - Project (code + report): 30% (deadline: May 10th, 6pm)
  - _DevOps & Continuous Testing_ : https://github.com/collet/isa-devops/blob/master/DevOps/README.md
    - Intermediate demonstration (technical interview): 20%	
    - Final demonstration (technical interview): 35%
    - Individual question (during tech interview): 15%
    - Project (code): 30% (deadline: May 10th, 6pm)

## Tooling

  - J2E environment: Apache TomEE+
  - Integration testing: Arquillian
  - .Net development: Mono
  - Containers: Docker
  - Continuous integration: Jenkins
  - Repository: ArtiFactory
