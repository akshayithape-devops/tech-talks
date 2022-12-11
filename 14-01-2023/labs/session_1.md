## Docker Session I - Hands-On Labs

### Prerequisite

---

Following are the prerequisite for the Hands-On Session.

#### 1. Create a Docker Hub id

Visit https://hub.docker.com/signup - use your personal email

#### 2. Verify Email Address

You will receive an email to confirm the Docker Hub account, once confirmed, your account is created with Docker Hub.

#### 3. Accessing Docker Lab

This is a free online lab environment for Docker, you can access it using the Docker Hub account create using the above steps, 

visit https://labs.play-with-docker.com/ and click on Login. 

This will open up a pop-up for login, ensure you don’t have pop-up blocker enabled in your browser. 

Once logged in with Docker, you should see the start button, click on Start

#### 4. Add a Docker Instance

Click on ‘ADD NEW INSTANCE’ label under Instance in the left hand side navbar. This will spawn up a docker instance for running lab tasks.

> Congratulations ! You have successfully setup your lab. You can click on close session if you want to close the lab.

---

### Hands-On Labs

### Lab 1 : Run your first container

1. Run a container
2. Run multiple containers
3. Remove the containers

#### 1. Run a container

- Verify version of docker
```
docker --version
```

- List docker images
```
docker images
```

- Search docker image for Webserver(Apache HTTPD)
```
docker search httpd
```

- Pull Apache HTTPD docker image
```
docker pull httpd:latest
```

- Verify that Apache HTTPD docker image is pulled successfully or not
```
docker images
```

- Run first container called `containerA`
```
docker run -d -p 8080:80 --name containerA httpd:latest
```

- List running Docker processes
```
docker ps
```

- Test the webserver is deployed in a container or not 
```
curl http://localhost:8080
```

#### 2. Run multiple containers

- Search for `hello-world`
```
docker search hello-world
```

- Pull hello-world docker image
```
docker pull hello-world:latest
```

- Verify that hello-world docker image is pulled successfully or not
```
docker images
```

- Run second container called `containerB`
```
docker run --name containerB hello-world:latest
```

- List running Docker processes
```
docker ps
```

- List all docker processes
```
docker ps -a
```

#### 3. Remove the containers

- List all docker processes
```
docker ps -a
```

- Stop running container
```
docker stop containerA
```

- List all docker processes
```
docker ps -a
```

- Remove all containers
```
docker rm containerA containerB
```

- Verify whether docker containers removed or not 
```
docker ps -a
```
