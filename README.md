<h1><img height="24" src="https://cdn.technicpack.net/platform2/pack-icons/1540031.png"/> EV.TECHNICS</h1>

[![](https://img.shields.io/badge/ON-TECHNICPACK.NET-cyan?style=for-the-badge)](https://www.technicpack.net/modpack/evtech)

## General Information

Evolved Technics is our personal take on the popular modpack Tekkit Lite. It is based on Minecraft 1.12.2 with every important mod updated to its new and fresh version. Some additional new mods help to enrich the gameplay and to improve the performance of the pack, while we want to ensure the same feel and taste like it used to be in Tekkit Lite.

## What is this Repository for?

This repository has two main purposes:

First of all, this repository holds all binary files, configurations and assets of the modpack server. This makes it way easier to maintain the modpack, pushing new versions and backuping old versions of the modpack.

Also, we are using [GitHub Actions](https://github.com/evolvedpacks/pack-client-evolved-technics/actions) to build and deploy releases of the modpack. Everytime a new version is created by setting a new [tag](https://github.com/evolvedpacks/pack-client-evolved-technics/tags), a CD *([Continous Deployment](https://en.wikipedia.org/wiki/Continuous_deployment))* process is started which creates a release bundle of the modpack server *(one as zip file and another one as tar.gz)*, creates a [Release](https://github.com/evolvedpacks/pack-client-evolved-technics/releases) in this repository where the bundles can then be downloaded from, and pushes the latest zip bundle to a CDN file server which then is utilized by technicpack.net to download the modpack bundle via the technic launcher.  
Also, a [Docker](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/container-docker-introduction/docker-defined) image is created which can be pulled to set up a server instance using the Docker engine. The images are hosted on [DockerHub](https://hub.docker.com/r/evolvedpacks/evt/tags?page=1&ordering=last_updated), so you can simply pull them from there, for example by using the `docker pull` command:
```
$ docker pull evolvedpacks/evt:latest
```

And all of this happens fully automatically without having to lift a finger.

If you are interested in how all of this is configured, take a look in the [workflow configuration file](https://github.com/evolvedpacks/pack-server-evolved-technics/blob/master/.github/workflows/tags-cd.yml) where all job steps are specified in.

