TO build and start application:
> cd 02.\ simpleweb
> docker build -t rajarz/simpleweb .
> docker run -p 8080:8080 rajarz/simpleweb
Note the above command will route incoming source machine requests (localhost port) to the container's port.


Copying into a nested directory on container filesystem, so that we don’t accidentally copy our lib
and overwrite the lib of the docker linux filesystem.
Hence, we create a WORKDIR “working directory” in a path is accepted to be safe to use in community.


To check the working directory folder, in another terminal type the below commands:
> docker exec -it <container id> sh

--
Notes
--

FROM node:alpine
Alpine suffix with node means you're getting a bare bones, or most compact version of node.
Wouldn't have things like git included, etc.



