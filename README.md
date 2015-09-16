# docker-sensu-client

A docker container with a Sensu client to send information about the host system to a Sensu server.

Best used with [docker-sensu-server](https://github.com/testobject/docker-sensu-server).

## Instructions

Assuming your Sensu server container is called "sensu-server"

    $ docker build -t sensuclient
    $ docker run -d --name sensu-client --link sensu-server \
	       sensuclient sensu-server CLIENT_NAME CLIENT_IP
	     
