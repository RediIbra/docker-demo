# docker-demo

Using docker to create containers with node versions

<b> You can use these commands in this project to learn Docker by yourself too. </b>

-docker images =>get all the imagines <br>
-docker ps -a =>get all containers (running and not running)<br>

//IMAGES <br>
-docker build -t myapp:nodemon . => create an image of actual code with tag (after : is the tag you want to use) <br>
-docker rmi myapp =>remove an image (You can't remove it if it's being used by a container; otherwise, use flag -f.) <br>

//CONTAINERS <br>
-docker run --name myapp_c1 myapp => create a container <br>
-docker start myapp_c =>start the container <br>
-docker stop myapp_c =>stop the container <br>
-docker rm myapp3 =>remove a container (you cant remove container if it is running ) <br>

//VOLUMES <br>
-docker run --name myapp_c_nodemon -p 4000:4000 --rm myapp:nodemon => CREATE a running container -p stands for maping the port and --rm remove container after we stop it <br>
-docker run --name myapp_c_nodemon -p 4000:4000 --rm -v C:\Users\r.ibra\Desktop\docker-demo\api:/app -v /app/node_modules myapp:nodemon => RUN changes in real time without node modules <br>

//DOCKER-COMPOSE <br>
-docker-compose up =>Run the docker-compose.yaml file we created and create image container and volumes <br>
-docker-compose down => Stop container created and delete <br>
-docker-compose down --rmi all -v => Stop the container and also delete images and volumes created <br>
