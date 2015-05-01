## Overview

Creates an OpenResty nginx container (with Lua module) that round-robins to two webserver containers.

* Run via `docker-compose up` to bring up containers.

* In browser, head over to http://DOCKER_HOST_IP:9000 and each refresh will round-robin you to a different web server.

* Try http://DOCKER_HOST_IP:9000/lua route to see the Lua module in action.

See below if you need more help setting up Docker and Docker Compose, and starting up Docker.

## Install on OSX

    # install Docker
    brew install boot2docker
    boot2docker init

    # install Docker Compose
    curl -L https://github.com/docker/compose/releases/download/1.2.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose

## Run

    # run docker via
    boot2docker up
    $(boot2docker shellinit)

    # run docker compose
    docker-compose up

    # show running instances
    docker-compose ps

    # to rebuild containers after making changes
    docker-compose build

## To connect to an exposed port, say in the browser

Say you've exposed port 9000 externally, and you want to view in the browser.
On OSX, find out what your DOCKER_HOST env is set to, say tcp://192.168.59.103:2376
In the browser, go to 192.168.59.103:9000


## More info

* http://openresty.org/

* https://github.com/torhve/openresty-docker
