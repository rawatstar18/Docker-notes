# docker registry 
1) a storage and distribution system for docker images.
2) official images available from applicaton like mongodb , redis , postgres 
3) these official images are maintained by the software authors or in collaboration with docker community.
4) docker hosts one of the biggest docker registry called 'docker hub'
5) as technology changes new version are out, new docker images were create hence docker images are versioned called tags.
6) latest tag is used for latest version.
7) using the specific version is the best practice.

# docker commands 

docker images                           --list docker images 
docker ps                               --list running docker container
docker ps -a                            -a or --all list all the container (running and stopped)
docker start <docker-id>                -- to restart the stooped container

# docker pull to dowload the docker images 
docker pull nginx:1.23        #docker pull <image_name>:<version/tag>
- docker pull images automatically, if image  

# docker run to run the container 
docker run -d <images_name>:<version/tag>   #-d refer to run in background 

# docker log 
docker logs <docker-id>
docker logs <docker-name>

# docker stop 
docker stop <docker-id>

# docker port bind 
1) Application inside run in an isolated network. 
    - we need to expose the container port to host.
2) port binding - bind the container'port to host's port to make the services available to outside world. 
 
    - We can do this binding while running the container by adding flag -p or --publish = publish a container port to host.

    - docker run -d -p 8080:80 nginx:1.23   #docker run -d -p{host_port}:{container_port}
    
    # Note: only one service can be host on a specific port on the host

# You can give the container name by using flag --name

docker run --name Pankaj -d -p 8080:80 nginx:1.23


