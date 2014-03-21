= Do it manually =

All docker cli commands: http://docs.docker.io/en/latest/reference/commandline/cli/

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
