---
title: "How to host Docker"
date: '2025-09-07 08:26:48 -0700'
tags:
  - self hosted
  - docker
  - ubuntu
  - linux
  - howto

layout: post
excerpt: I keep running around in circles with docker hosting.  Mac OS X, Ubuntu, REHL, Docker in an LXC, Docker in a VM, bare metal.  What is the perfect setup?
feature-img: /assets/img/feature-img/dock.png
thumbnail: /assets/img/feature-img/dock.png
bootstrap: true
published: false
---
# How to Host Docker

I have hosted a lot of stuff on a lot of system.  Over the years of course I settled on docker as the way to setup applications and services on servers.  But how do you host docker?  I have hosted with docker desktop.  Moved to docker on VM's then shrink it to docker on LXC containers.  I hae used Mac OS X, Ubuntu, Red Hat all sorts of hosts.  In the end I have I circled back to Ubuntu systems.  In the enterprise world we setup servers with code but at home going to effort of building a server for managing servers is a little overkill.  Most people just want to set something up and go.  How do we setup and go without building repeatable infrastructure like ansible.  The answer is shell scripts.

Instead of telling you how to setup a server for docker, I am posting a script to setup a server for docker.  ubuntu_docker_setup.sh.  Copy it onto server on your first login and run it!  The script installs neofetch because I like the server telling me what it is when I log in.  Docker gets installed and portainer to manage docker.  Not only does it install portainer the script creates a docker directory for the various docker containers a folder inside that directory for portainer and builds a docker-compose.yml for portainer then stands up portainer using docker compose.  So by using the script you are all setup with an example of how to manage docker with code instead of trying to do everything with portainer or trying to launch containers with the docker command.

Here is the [script](https://github.com/mjh2901/ubuntu_docker_setup.githttps:/)
https://github.com/mjh2901/ubuntu_docker_setup.git
