

CJP Local QA Lab
----

This repo contains several Docker Compose configurations for testing
various things with the CloudBees Jenkins Platform. Docker Compose is
useful because you can startup up several related Docker images as a
unit without writing a bunch of shell scripts to manage these.

With any luck, we can additional write Docker Compose configurations
to make it easy to setup things like HA, Elasticsearch and
integrations with other Linux-based services (LDAP comes to mind).

Getting Started
----

1. Install [Docker Engine](https://www.docker.com/docker-engine) if you
  are on Windows or OS X. This will install docker-machine,
  docker-compose & docker. A working docker-compose is the real
  requirement here.

2. Create the Docker Machine if you are on OS X or Windows: 

    $ docker-machine create --driver virtualbox mymachine

3. Tell your Docker client to talk to that Docker Machine (not sure
    about Windows syntax): 

    $ eval $(docker-machine env mymachine)

4. Change your working directory to one of the subdirectories
   contained herein. 

    $ cd cjoc-basic

5. Start the configuration. This will download the needed images and
   start them up in the background. 

    $ docker-compose -d up

6. You can find the Docker Machine address: 

    $ docker-machine ip mymachine

6. Look at the logs of the running containers.

    $ docker-compose logs

7. Stop the configuration

    $ docker-compose stop

8. Learn more

    $ docker-compose -h
