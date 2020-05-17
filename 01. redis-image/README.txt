
TO RUN PROGRAM:
cd 01.\ redis-image
docker build .

To Tag image using community convention, you can type alernate build command:
> docker build -t rahul/redis:latest

--
Notes
--

First example of running docker:
> docker run hello-world

To see that Docker running a linux virtual machine:
> docker version
"OS/Arch:   linux/amd64"

Showcasing a default command to execute after container has been loaded through run
> docker run busybox echo hi there
> docker run busybox ls
> docker run busybox ping google.com

List all running containers
> docker ps

Listing of all containers ever created
> docker ps --all

Get logs from a container
> docker logs <container_id>

Stop a Container:
Note usually Docker will kill if app doesn't respond within some number of seconds.
> docker stop <container_id>

Kill a Container:
> docker kill <container_id>

Will delete docker containers including;
- All stopped containers, all dangling images, all build caches (so will have to re-download images like hello-world)
> docker system prune

Stuff you type into terminal will get directed to docker process and back out to terminal if you include -IT flag
> docker exec -it <container_id> sh
# ls

Tagging an image (so you don't have to reference the container id)
Convention to use: docker run <DockerId>/<Repo/ProjectName>:Version
> docker run stephengrider/redis:latest