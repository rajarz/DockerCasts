Note that code has been moved to:
/Users/rahulrajaram/Documents/GitHub/docker-projects/docker-react


INSTRUCTIONS TO BUILD AND RUN MANUALLY:

First build dockerfile:
> docker build -f Dockerfile.dev .

To get the image id, find right at the end of the terminal:
"Successfully built b89fd18d73f3"

Then to run within a Docker Volume:
docker run -p 3000:3000 -v /app/node_modules -v "$(pwd):/app" b89fd18d73f3

(PREFERRED) INSTRUCTIONS TO RUN USING DOCKER COMPOSE:

> docker-compose down && docker-compose up --build

----

Application could be accessed from:
http://docker-env.eba-u8xmrw2f.ap-southeast-2.elasticbeanstalk.com/

