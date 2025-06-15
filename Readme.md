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
- Docker helps in creating containers, that reduce the hectic way of installing softwares GUI and  fill your computers with the unneccessary softwares, instead it provides you a container which has everything built in, and you can access everything just by a single command. 

## You can push IMAGES to DOCKER REGISTRIES
- Image => Anything you want to expose to the world, for other developers as well. 
- First the image is being created. It is basically a CD drive kind of thing. 
- You can get the images for the registeries locally in your machine. (Dockerhub)
- Image in EXECUTION is called a container.