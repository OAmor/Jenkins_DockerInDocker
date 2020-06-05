# Jenkins_DockerInDocker Get Started
The DID concept (docker in docker) is to integrate the VM docker inside the container 
if the volume is new then the default generated password will be displayed in the execution log 

1. cd into project and build Jenkins image by running  
`docker build -t jenkins .`

2. we need to create a docker volume to persist the data using
```docker volume create jenkins_volume```

3. now we can run the container by
```
docker run -p 8080:8080 -p 50000:50000 -v jenkins_volume:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock jenkins
```

4. The dashboard will be available at :8080 

Enjoy :) 
