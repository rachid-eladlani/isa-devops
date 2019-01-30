# DevOps & Continuous Testing (2018-19)

## Teaching Staff

  * [Guilhem Molines](guilhem.molines@univ-cotedazur.fr), IBM France Lab, Université Côte d'Azur (co-head, DevOps)
  * [Salah Dahmoul](Salah.DAHMOUL@univ-cotedazur.fr), Orange, Université Côte d'Azur (DevOps)


## Lecture Material

  - Lecture #1: [DevOps Overview]
  - Lecture #2: [Architecture For Testing]
  - Lecture #3: [Functional & Integration Testing]
  - Lecture #4: Continuous Integration
    - 4.1: [Part one]
    - 4.2: [Part two]
  - Lecture #5: [Deployment]
  - Lecture #6: [Software Containers]
  - Lecture #7: Scaling


## Previous exams (FR)

  - [2016](https://github.com/collet/isa-devops/blob/master/DevOps/exams/examen2016.pdf)
  - [2017](https://github.com/collet/isa-devops/blob/master/DevOps/exams/examen2017-2.pdf)

## Deliverables

### First release of the project

### Final release of the project

We will checkout your code in the main repository, with the git options to extract the tag `XXXXXXXX` and to follow sub-modules.

Once done, we will launch the script `build.sh` that you will have placed at the root of this extraction. This scripts should trigger a full build of everything all the way to the docker images of your project. Our evaluation machines have (at least) bash, maven, python, ant, perl, docker on them. Should anything else be required for the script to run, then the script has to say it.

Once the script finishes successfully, we will launch the script `run.sh` which you will have provided. This script is supposed to launch your project (database, dependents, server), most likely with a `docker-composer up` command.

Once this script finishes, we assume the server is up, we will then open the file `scenarios.md` placed at the root of your directory, which should guide us through what to do to run the scenarios.
In a separate terminal, we will launch the script `client.sh` to launch the CLI client, and we will follow the scenarios described in the `scenarios.md` file to run through the demo ourselves.

Finally, we will launch the script `jenkins.sh`, which you should set up so that it launches a jenkins docker container pointing to a volume located in one of the sub-directories of your git repository, in which you will have copied the content of the volume you use as a data storage of your current jenkins. This way, we'll be able to point a browser at this jenkins instance and browse your build plans to check how they are setup.
