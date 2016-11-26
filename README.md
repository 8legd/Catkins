# Catkins

Containerised [Jenkins](https://jenkins.io/) supporting containerised builds i.e. you can use Docker Compose in your builds

This fork of the official Jenkins Docker image no longer runs under UID 1000 (which can cause permission problems e.g. if you bind mount a volume for `jenkins_home`) and adds some basic build tools and Docker Compose to the container

Docker itself can be made accessible through bind mounting - i.e. by adding the following volumes in docker-compose.yml
```
  - /usr/bin/docker:/usr/bin/docker
  - /var/run/docker.sock:/var/run/docker.sock
```
