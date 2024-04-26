### Step to run docker
1. Install docker desktop from https://www.docker.com/products/docker-desktop (download for windows)
2. open docker desktop 3.Sign in to docker desktop with docker hub credentials

3. Open command prompt and run below command
```shell
docker --version
```

4. In the project directory, create a Dockerfile
5. Add below code in Dockerfile
```shell
FROM openjdk:21

COPY target/testdocker-0.0.1-SNAPSHOT.jar app.jar

ENTRYPOINT ["java", "-jar", "app.jar"]

```
6. from terminal, run below command
```shell
docker build -t kmeera/testdocker:v0.000001 .
```
kmmera = username, testdocker = repository name, v0.000001 = tag name
7. Run below command to test
```shell
docker run kmeera/testdocker:v0.000001
```
8. Run below command to push the image to docker hub
```shell
docker push kmeera/testdocker:v0.000001
```
9. deploy docker container to port 8080
```shell
docker run -p 8080:8080 -d kmeera/testdocker:v0.000001
```

