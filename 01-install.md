# 1) Installation


## Virtualbox image
* Have https://www.virtualbox.org/ installed
* Install and start the workshop VM:

  `docker-workshop_docker-workshop-vm_*.ova`
* Double Click or Virtual Box > File > Import Appliance ...
* Login: `ssh -p 2222 demo@localhost` Password: demo
  ```
  $ ssh -p 2222 demo@localhost
  demo@localhost's password:
  Welcome to Ubuntu 14.04 LTS (GNU/Linux 3.13.0-24-generic x86_64)
  ...
  ```


## docker version

```
  $ docker version
  Client version: 1.3.0
  Client API version: 1.15
  Go version (client): go1.3.3
  Git commit (client): c78088f
  OS/Arch (client): linux/amd64
  Server version: 1.3.0
  Server API version: 1.15
  Go version (server): go1.3.3
  Git commit (server): c78088f
```


## docker info

```
  $ docker info
  Containers: 1
  Images: 49
  Storage Driver: devicemapper
   Pool Name: docker-8:1-262794-pool
   Pool Blocksize: 65.54 kB
   Data file: /var/lib/docker/devicemapper/devicemapper/data
   Metadata file: /var/lib/docker/devicemapper/devicemapper/metadata
   Data Space Used: 1.485 GB
   Data Space Total: 107.4 GB
   Metadata Space Used: 2.306 MB
   Metadata Space Total: 2.147 GB
   Library Version: 1.02.82-git (2013-10-04)
  Execution Driver: native-0.2
  Kernel Version: 3.13.0-24-generic
  Operating System: Ubuntu 14.04 LTS
  WARNING: No swap limit support
```


## docker help

```
$ docker help
Usage: docker [OPTIONS] COMMAND [arg...]

A self-sufficient runtime for linux containers.

Options:
  --api-enable-cors=false                    Enable CORS headers in the remote API
  -b, --bridge=""                            Attach containers to a pre-existing network bridge
                                               use 'none' to disable container networking
...
Commands:
    attach    Attach to a running container
    build     Build an image from a Dockerfile
    commit    Create a new image from a container's changes
    cp        Copy files/folders from a container's filesystem to the host path
    create    Create a new container
...
```


## Local Docker registry

```
# start a local registry
$ /usr/local/bin/start_registry.sh
```

```
# check local registry
$ docker ps -a
CONTAINER ID        IMAGE                         COMMAND                CREATED             STATUS                       PORTS                      NAMES
5bb7620b2b47        registry:latest               "/bin/sh -c 'exec do   14 minutes ago      Up 14 minutes                127.0.0.1:5000->5000/tcp   registry
```


## Excercise 1

1. Check your Docker installation.
2. Examine available Docker commands. 


## More Information

* Google! Everything get's outdated very fast.
* http://www.dockerbook.com/
* Cheat-sheet for commands:<br> https://github.com/wsargent/docker-cheat-sheet
