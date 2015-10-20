# docker-sensu-client

A docker container with a Sensu client to send information about the host system to a Sensu server.
If it runs --privileged, it will run ntpd to keep the system time up to date. This is important
on a Sensu client, as if the time drifts out of sync with the server then Sensu will think the
keepalives are being sent at the wrong time and alerts will go off.

Best used with [docker-sensu-server](https://github.com/testobject/docker-sensu-server).

## Instructions

    $ docker build -t sensuclient
    $ docker run -d --privileged --name sensu-client \
	       sensuclient HOST_IP CLIENT_NAME CLIENT_IP
	     
