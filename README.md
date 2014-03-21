= Test it manually =

Install Docker (http://docs.docker.io/en/latest/installation/ubuntulinux/#ubuntu-raring-saucy)

    sudo apt-get install linux-image-extra-`uname -r`
    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9
    sudo sh -c "echo deb http://get.docker.io/ubuntu docker main > /etc/apt/sources.list.d/docker.list"
    sudo apt-get update
    sudo apt-get install lxc-docker

All docker cli commands: http://docs.docker.io/en/latest/reference/commandline/cli/
All docker images: https://index.docker.io/u/paulczar/chef-client/

Run a command in a new container built from image

    sudo docker run -i -t ubuntu:12.04 /bin/bash

In another Terminal

    sudo docker ps
    sudo docker commit -m "Create demo image" [CONTAINER_ID] demo
    sudo docker images

In the first terminal. Run container from previously created container

    exit
    sudo docker run -i -t demo /bin/bash
    exit

Save into a tar

    sudo docker save demo > demo.tar

Load image from a tar

    sudo docker load < demo.tar

= Tutorials =

* http://hotcashew.com/2013/07/lemp-stack-in-a-docker-io-container/
* http://tech.paulcz.net/2013/09/creating-immutable-servers-with-chef-and-docker-dot-io.html
* https://index.docker.io/u/paulczar/chef-client/

* https://ochronus.com/docker-primer-django/
