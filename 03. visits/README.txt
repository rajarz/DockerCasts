
Docker Compose is a CLI command that:
- Is used to startup multiple Docker containers at the same time.
- Automates some long-winded arguments that were passed to 'docker run`

Previously, we would run:
> docker build -t rajarz/visits:latest
> docker run -p 8080:8080 rajarz/visits

Now we run:
> docker-compose up --build

To view the application in Chrome:
http://127.0.0.1:4001/

----

To rebuild an image i.e. equivalent of running below 2 commands:
> docker build.
> docker run myImage

Rebuild command below:
> docker-compose up --build

To stop multiple containers:
> docker-compose down

** To knock down and rebuild:
> docker-compose down && docker-compose up --build