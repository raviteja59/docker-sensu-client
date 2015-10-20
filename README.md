# docker-sensu-client

A docker container with a Sensu client to send information about the host system to a Sensu server.

Best used with [docker-sensu-server](https://github.com/testobject/docker-sensu-server).

## Instructions

    $ docker build -t sensuclient
    $ docker run -d --name sensu-client \
	       sensuclient HOST_IP CLIENT_NAME CLIENT_IP
	     
