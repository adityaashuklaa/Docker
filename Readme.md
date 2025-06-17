# Learning Docker

> This is the repo i have created for my own learning, which cover the concepts of docker and notes along with it. 

## Steping stone to Kubernetes 
- If you want to run processes in isolated environments, Docker(Containers) let you do so! 
- The benefit of using docker is that the isolated environments cannot talk to eachother and independent.
- If you have one isolated environment you can run 10 different applications on them.
- Starting projects locally/ auxillary services locally.
- Auxilary Services => Postgress

## Containerization in Docker  
- A container is an enviroment, or mini machine working on your main machine. 
- Container is a way to package and distribute software applications in a way that makes them easy to deploy and run consistently across different environments.
- Runs on any machine and runs consistently.

## Example for starting a MongoDB Container
- docker run -d -p 27017:27017 mongo 
- docker is not the only way to create containers, just a popular choice among developers.  
- Docker helps in creating containers, that reduce the hectic way of installing softwares GUI and  fill your computers with the unneccessary softwares, instead it provides you a container which has everything built in, and you can access everything just by a single command. 

## You can push IMAGES to DOCKER REGISTRIES
- Image => Anything you want to expose to the world, for other developers as well. 
- First the image is being created. It is basically a CD drive kind of thing. 
- You can get the images for the registeries locally in your machine. (Dockerhub)
- Image in EXECUTION is called a container.

## Common commands
- docker run (name of file)
- docker ps 
- docker kill

## Port Mapping
- docker run -p 27017:27017 mongo 
- This command will map the machine port to the container port of the mongo image.
- If you don't want to see any logs, you can run the docker to the detach mode by running the command : 
docker run -d -p 27017:27017 mongo
- docker ps command shows the current containers being running
- If you want to stop the container just run the command docker kill (container ID)

## For starting Postgres
- This is the command to start postgres locally on your machine. 
- docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres  
- -e is for environment variables that is being used to create environment.
- docker run {containerID} is the command to run a container

## Docker Kill
- docker kill {contaainerId} => this command will kill the container
- To remove the image docker rmi {image name} command is being used. 

## DockerFile
- If you want to create an image from your own code, that you can push to dockerhub, you need to create a dockerfile for your application.
- A Dockerfile is a text document that contains all the commands a user could call on the command line to create an image. 

## Basic Boiler Plate Code for Docker File
- FROM node:16-alpine  ==> Base Image
- WORKDIR /app ==> Defining Path for Working Directory.
- COPY .. => This commands takes two argument, First argument is the files of the src directory and copy it to the Working Directory. First argument is basically every files, you can see by doing ls.
- RUN npm install
- RUN npm run build - This is the run command which builds the code.
- EXPOSE 3000 - Expose Ports
- CMD ["node", "dist/index.js"] => Final command that runs while running the container.

- Run command is used to boostrapping the resources like installing node and express, while CMD is used to actually run the containers.


- ![Example Image](image.png)