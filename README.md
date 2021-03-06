# OPENROAD_USERS_READ_ME_FIRST
OpenROAD users should look at this repository first for instructions on getting started.

New users should not try to build the individual repo's from their master branches.
With the advent of the [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD) unified application, all of the needed code is built directly there.
The individual repos' master branches should be considered legacy code.

New users should start by following the directions in the [OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) repo's [flow README](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts/blob/master/README.md).
The procedures for the download of prebuilt binaries, building all of the code in a container, and building all of the code on bare metal are described there.
The application submodules all point to stable and tested versions of code.
The [OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) repo also contains open source sample designs on an open source PDK.
Along with these designs are Makefiles to run the designs through OpenROAD.

OpenROAD is comprised of a set of repos, however they are all integrated into the top level application repo named [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD) except for Yosys and TritonRoute which will be integrated soon.
All of the repos that the OpenROAD top level applications needs are set up as sub modules.
The top level cmake configuration builds all of them.
Be sure to clone openroad with the --recursive option to clone all of the submodules in preparation for building.
If you follow this procedure and the rest of the instructions as specified in the [application README](https://github.com/The-OpenROAD-Project/OpenROAD/blob/master/README.md) you will be able to build the application and all of its submodules.
Keep in mind that you will need to have the build tools in place that are required for building.
If you wish to use docker you can use the image provided here for [Centos7](https://hub.docker.com/r/openroad/centos7-dev) or [Ubuntu 20.04](https://hub.docker.com/r/openroad/ubuntu20-dev) -- to build a local image see `./etc/DockerHelper.sh -help`.
The `./etc/DependencyInstaller.sh` [here](https://github.com/The-OpenROAD-Project/OpenROAD/blob/master/etc/DependencyInstaller.sh) script installs the dependencies needed to build the app -- the script supports Centos7 and Ubuntu 20.04 and requires root access.

A architecture [guide](https://openroad.readthedocs.io/en/latest/contrib/OpenroadArch.html) which explains the philosophy behind the code organization and architecture and also describes the workflow for developers to follow is available.
Working with submodules in git is non trivial.
If you follow the procedures in the section marked Tool Work Flow, you will have a streamlined way to work efficiently.

More information can be found on our project [website](https://theopenroadproject.org/).

Please also follow us on [twitter](https://twitter.com/OpenROAD_EDA) to be notified of important project developments.

Please also "star" our project and repos so we know how many people are interested in what we do!
