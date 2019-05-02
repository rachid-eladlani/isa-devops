# Second Demonstration

  * Date: 03.05.19
  * Examiners: Philippe Collet (PC), Laureen Ginier (LG), Guilhem Molines (GM), Anne-Marie Pinna-Déry (AMD), Salah Dahmoul (SD)

## Planning

  * Constraints: 
    * 15 minutes for the team, 15 minutes from the jury;
    * No slides;
    * Live demonstration (no video)

  * Planning: 
 
| Timeslot      | O+109 (PC, LG, GM, AMD, SD)  | 
|---------------|---------|
| 08:00 - 08:30 | Team J  | 
| 08:30 - 09:00 | Team K  | 
 
| Timeslot      | O+109 (LG, GM, SD) | O+110 (AMD, PC) |
|---------------|---------|---------|
| 09:15 - 09:45 | Team A  | Team F  | 
| 09:45 - 10:15 | Team B  | Team G  | 

| Timeslot      | O+109 (AMD, GM, SD) | O+110 (LG, PC) |
|---------------|---------|---------|
| 10:30 - 11:00 | Team C  | Team H  | 
| 11:00 - 11:30 | Team E  | Team I  | 
| 11:30 - 12:00 | Team D  |  | 


## Expectations

You have to demonstrate a single product, covering both ISA & DevOps course contents. This single demo will be evaluated according to these two dimensions, leading to two different marks. *However*, the two courses expect the project to respect the _PolyDiploma_ call for bids and implement features related to this project.

Think about demonstrating error cases (e.g., third party service unavailable, network lost, broken test, corrupted JAR, ...) instead of staying in a perfect world. 

  * For *ISA*, the keypoint is to demonstrate a comprehensive architecture, going from the persistence layer to the exposition one (_i.e._, web services, CLI or other interface). You must be able to defend the strengths of your architecture, as well as discuss its limitations and evolution capabilities. You can follow the previous points put on the slack:
     * presentation for the evolution of the architecture, its decomposition into components, and what has changed from the MVP of the 1st demo (scenarios, new clients, external services, new or evolution of stateless/ful components)
     * explanation of the impact of the integration of persistence
     * Where and why did you integrate communication by messages (or where/why it could have be done, if you did not have time to do so)
     * Where and why did you integrate interceptors (or where/why it could have be done, if you did not have time to do so)
  * For *DevOps*, you demonstrated during the first demo that you master a Continuous Integration system. For demo 2, we expect to see a Continuous Delivery system. By that, we mean to see a fully instrumented pipeline, that not only compiles the code, but also proves it correct through various level of testing and generates the product deliverables. We expect the core product deliverable to be in the form of (at least two) docker images, and launchable through a simple command line [we do not place the docker requirement on the clients and the external servers, but launching them should be trivial as well]. Docker Compose is not mandatory, but strongly advised. There is no requirement on any scaling technology such as Swarm or Kubernetes. Be ready to answer questions on your testing and branching strategies.

You must also clearly identify who did what (for both topics) in the project development.
