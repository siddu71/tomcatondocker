# tomcatondocker
how to install tomcat on docker

```
cat >>Dockerfile
```

Copy the following 
```
FROM tomcat:8.0-alpine

LABEL maintainer="siddarthsiddu71@gmail.com"

EXPOSE 8080

CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]
```
Build the image by running docker build command
```
docker build -t tomcat-server .
```
check images 
```
docker images
```
Run the docker images using docker run command
```
docker run -d -p 8080:8080 tomcat-server:latest
```
check docker containers usisg 
```
docker ps -a 
```
Access in browser using 
```
https://<instanceip>:8080
```
![image](https://user-images.githubusercontent.com/52039971/198987719-ba0e3855-0fb5-4b70-a8e9-c37765e44db8.png)

