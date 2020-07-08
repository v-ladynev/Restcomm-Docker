# RestComm Docker image

## Build

To build the image:

1. git clone this repository

2. if you are using Windows check that all shell scripts have `LF` line separators

3. run this command from the root of this project to build `restcomm/restcomm` image. Make sure you don't skip the dot (.) at the end of the command
```bash
docker build -t restcomm/restcomm:latest -f Dockerfile .
```
Parameters explanation

`-t` Name and optionally a tag in the 'name:tag' format (`restcomm/restcomm:latest`)

`-f` Docker file to use for build the container (`Dockerfile`)

## Run

1. run Restcomm application using `docker-compose` from the root  
```bash
docker-compose up
```
2. login using URL http://localhost:8080/

3. enter default credentials
```
username : administrator@company.com
password : RestComm  
```
