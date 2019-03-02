About
-----

**NGINX** running as webserver in a _non-root_ docker container that
serves a simple page containing the container's hostname, IP address and port
Running in OpenShift Container Platform, OpenShift Online, and OpenShift dedicated requires that your container be able to run as a random non-admin userid.

Based on:
 - https://github.com/nginxinc/NGINX-Demos/tree/master/nginx-hello
 - https://github.com/nginxinc/docker-nginx


The images are uploaded to Docker Hub -- https://hub.docker.com/r/shiwaforce/openshift-nginx-hello.

How to run:
```
$ docker run -P -d shiwaforce/openshift-nginx-hello
```

Now, assuming we found out the IP address and the port that mapped to port 8080 on the container, in a browser we can make a request to the webserver and get the page below: ![hello](https://raw.githubusercontent.com/shiwaforce/openshift-nginx-hello/master/hello.png)

The images were created to be used as simple backends for various load balancing demos.
