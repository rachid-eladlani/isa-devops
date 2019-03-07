# DevOps & Continuous Testing (2018-19)

## Teaching Staff

  * [Guilhem Molines](guilhem.molines@univ-cotedazur.fr), IBM France Lab, Université Côte d'Azur (co-head, DevOps)
  * [Salah Dahmoul](Salah.DAHMOUL@univ-cotedazur.fr), Orange, Université Côte d'Azur (DevOps)


## Lecture Material

  - Lecture #1: [DevOps Overview](https://github.com/collet/isa-devops/blob/master/DevOps/week1_overview_devops.pdf)
  - Lecture #2: [Testing](https://github.com/collet/isa-devops/blob/master/DevOps/week2_testing_v0.2.pdf)
  - Lecture #3: [Artifactory](https://github.com/collet/isa-devops/blob/master/DevOps/week3_software_factory_v0.4.pdf)
  - Lecture #4: [Docker]
  - Lecture #5: [Multi-plan CI]
  - Lecture #6: [DevOps Dojo]
  - Lecture #7: [Compose]
  - Lecture #8: [Kubernetes]


## Assignment #1

First Assignment requires you to compile and package the code base of The Cookie Factory. The code base is available [in this zip file](https://github.com/collet/isa-devops/blob/master/DevOps/TDs/tcf_td1.zip).

## Assignment #2
Independant local compilation of two components

## Assignment #3
We'll use Artifactory to distribute the build. To run it:
`docker run --name artifactory-5 -d -v /your/home/artifactory:/var/opt/jfrog/artifactory -p 8081:8081 docker.bintray.io/jfrog/artifactory-oss:latest`
This will launch Artifactory as a background process, saving its data to the directory `/your/home/artifactory` so that the configuration is persisted between sessions.


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
