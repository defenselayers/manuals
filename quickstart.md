# Quickstart
This document describes first steps for new [Defenselayers](https://defenselayers.com)  user.

## Accessing Defenselayers registries

> Before getting access to any of the Defenselayers' secure harbour registries you need to register yourself.

There are 2 secure harbour registries [Defenselayers](https://defenselayers.com) with currently used hosts:

1. `production` hosting production-grade secure images at: registry.defenselayers.com
1. `developer` hosting beta stage secure images at: registry.defenselayers.dev

### Accessing registries with Docker or podman
[podman](https://podman.io/) provides the client command line interface compatible with [docker](https://www.docker.com/) . 

To use below examples with `podman` issue the following command first:

```bash
$ alias docker=podman
```

Then, to access/download [Defenselayers](https://defenselayers.com) secure container images follow the steps:

1. login to registry: `$ docker login registry.defenselayers.com` 
1. provide correct _username_ and _password_ you had received when registered with [Defenselayers](https://defenselayers.com)
1. after successful login download any of the available secure container images using: `$ docker pull` command (e.g. `$ docker pull registry.defenselayers.com/deflayers-base:latest`)

> In case you are not sure which tag to use, the `latest` tag comes handy.

> Please always add `registry.defenselayers.com/` prefix before any secure container image name. 

## Listing Defenselayers registries content
To easily and quickly list content of all Defenselayers registries we provide 
[shm](https://github.com/defenselayers/shm) command line tool.

`shm` is a shortcut of _secure harbour manifest_. 

### Installing shm
[shm](https://github.com/defenselayers/shm) requires [Python 3](https://www.python.org/) and `pip3`. Most Linux
distros come with `pip3` as a compiled package. 

On Debian/Ubuntu systems to install both required elements just type in:

```bash
$ sudo apt update
$ sudo apt -y install python3 python3-pip
```

To install shm clone, its repository and install it using `pip` (some distros install Python 3 pip as `pip3`) use:

```bash
$ git clone https://github.com/defenselayers/shm
$ cd ./shm
$ pip install .
``` 

For complete [shm](https://github.com/defenselayers/shm)  documentation refer to its
[README.md](https://github.com/defenselayers/shm/blob/master/README.md) file.

### Running shm
To run [shm](https://github.com/defenselayers/shm) type `shm` at the command line. With no switches it would
ask you for _username_ and _password_ and list all available secure images at `production` registry. 

> To have a detailed output including image tags (0.1 etc.) use `-v` (verbose switch):
> `$ shm -v`
