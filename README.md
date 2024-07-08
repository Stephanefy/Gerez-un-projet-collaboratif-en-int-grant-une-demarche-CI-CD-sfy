# BobApp

Clone project:



There are two ways to launch the app via Docker

## Launching the app by starting each containers with Docker

You can start containers individually by following the instructions below. 

> git clone XXXXX

### Front-end 

Go inside folder the front folder:

> cd front

Install dependencies:

> npm install

Launch Front-end:

> npm run start;

### Docker

Build the container:

> docker build -t bobapp-front .  

Start the container:

> docker run -p 8080:8080 --name bobapp-front -d bobapp-front

### Back-end

Go inside folder the back folder:

> cd back

Install dependencies:

> mvn clean install

Launch Back-end:

>  mvn spring-boot:run

Launch the tests:

> mvn clean install

### Docker

Build the container:

> docker build -t bobapp-back .  

Start the container:

> docker run -p 8080:8080 --name bobapp-back -d bobapp-back 

## Launching the app with docker compose by starting multiple containers

Inside the root of the project

Run this command : 

> docker compose -up --build 

the --build option will ensure a fresh build of both containers

