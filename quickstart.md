# Quickstart
This document describes first steps for new [Defenselayers](https://defenselayers.com)  user.

## Accessing Defenselayers registries

> Before getting access to any of Defenselayers secure harbour registries you need to register yourself.

There are 2 secure harbour registries [Defenselayers](https://defenselayers.com)  current hosts:

1. `production` hosting production grade secure images at: registry.defenselayers.com
1. `developer` hosting beta stage secure images: at registry.defenselayers.dev

### Accessing registries with Docker or podman
[podman](https://podman.io/) provides compatible with [docker](https://www.docker.com/) client command line interface. 

To use below examples with `podman` issue following command first:

```bash
$ alias docker=podman
```

Now to access/download [Defenselayers](https://defenselayers.com) secure container images:

1. login to registry: `$ docker login registry.defenselayers.com` 
1. provide correct _username_ and _password_ you have received when registered with [Defenselayers](https://defenselayers.com)
1. after successfully login download any of available secure container image using: `$ docker pull` command (e.g. `$ docker pull registry.defenselayers.com/deflayers-base:latest`)

> If you are not sure which tag use, the `latest` tag is always available.

> Please note and always add `registry.defenselayers.com/` prefix before any secure container name image. 

## Listing Defenselayers registries content
To easily and quickly list content of all Defenselayers registries we provide 
[shm](https://github.com/defenselayers/shm) command line tool.

`shm` is a shortcut from _secure harbour manifest_. 

### Installing shm
[shm](https://github.com/defenselayers/shm) requires [Python 3](https://www.python.org/) and `pip3`. Most Linux
distros comes with `pip3` as compiled package. 

On Debian/Ubuntu systems to install both requirements just type:

```bash
$ sudo apt update
$ sudo apt -y install python3 python3-pip
```

To install shm clone its repository and install it using `pip` (some distros install Python 3 pip as `pip3`):

```bash
$ git clone https://github.com/defenselayers/shm
$ cd ./shm
$ pip install .
``` 

For complete [shm](https://github.com/defenselayers/shm)  documentation refer to its
[README.md](https://github.com/defenselayers/shm/blob/master/README.md) file.

### Running shm
To run [shm](https://github.com/defenselayers/shm) simply type `shm` from command line. Without any switches it will
ask you for _username_ and _password_ and list all available secure images at `production` registry. 

> To have a more detailed output including image tags (0.1 etc.) use `-v` (verbose switch):
> `$ shm -v`
