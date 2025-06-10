# Learning Docker

> This is the repo i have created for my own learning, which cover the concepts of docker and notes along with it. 

## Steping stone to Kubernetes
- If you want to run processes in isolated environments, Docker(Containers) let you do so! 
- The benefit of using docker is that the isolated environments cannot talk to eachother and independent.
- If you have one isolated environment you can run 10 different applications on them.
- Starting projects locally/ auxillary services locally.
- Auxilary Services => Postgress

## Containerization
- A container is an enviroment, or mini machine working on your main machine. 
- Container is a way to package and distribute software applications in a way that makes them easy to deploy and run consistently across different environments.
- Runs on any machine and runs consistently.

## Example for starting a MongoDB Container
- docker run -d -p 27017:27017 mongo 
- docker is not the only way to create containers, just a popular choice among developers.

