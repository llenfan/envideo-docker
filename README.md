# envideo-docker
# Basic usage:

###### 1- Clone repository
###### 2- Run the following commands:
    - docker-compose build
    - docker-compose up
###### 3- Test webserver/database on http://www.localhost
###### 4- from a new terminal purge www directory: rm ./www/* -r
###### 5- Get into www and clone envideo repository, configure and import database phpmyadmin http://localhost:8080/

### Docker Troubleshooting

###### Error: Bind for 0.0.0.0:3306 failed: port is already allocated

- docker stop $(docker ps -aq)
- docker rm $(docker ps -aq)

### Connect container with bash:

1) use "docker ps -a" to list all active containers
2) take container id from the CONTAINER_ID column i.g.: 3b6576a9f914
3) connect to that container shell with "docker exec -it 3b6576a9f914 /bin/sh"
4) do what you want
