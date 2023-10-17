# docker-demo

Using docker to create containers with node versions

docker images ->get all the imagines
/docker ps -a ->get all containers (running and not running)

//IMAGES
docker build -t myapp:nodemon . -> create an image of actual code with tag (after : is the tag you want to use)
docker rmi myapp ->remove an image (You can't remove it if it's being used by a container; otherwise, use flag -f.)

//CONTAINERS
docker run --name myapp_c1 myapp -> create a container
docker start myapp_c ->start the container
docker stop myapp_c ->stop the container
docker rm myapp3 ->remove a container (you cant remove container if it is running )

//VOLUMES
docker run --name myapp_c_nodemon -p 4000:4000 --rm myapp:nodemon -> create a running container -p stands for maping the port and --rm remove container after we stop it
docker run --name myapp_c_nodemon -p 4000:4000 --rm -v C:\Users\r.ibra\Desktop\docker-crash-course-lesson-5\api:/app -v /app/node_modules myapp:nodemon -> RUN changes in real time without node modules

//DOCKER-COMPOSE
docker-compose up ->Run the docker-compose.yaml file we created and create image container and volumes
docker-compose down -> Stop container created and delete
docker-compose down --rmi all -v -> Stop the container and also delete images and volumes created
