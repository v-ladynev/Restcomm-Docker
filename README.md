# RestComm Docker image

## Build

To build the image:

1. git clone this repository

2. if you are using Windows check that all shell scripts have `LF` line separators

3. run this command to build `restcomm/restcomm` image

```docker build -t restcomm/restcomm:latest -f Dockerfile .```

__Make sure you don't skip the dot (.) at the end of the command__

__-t Name and optionally a tag in the 'name:tag' format__

__-f Docker file to use for build the container__

Docker official links:
[Docker build manual](https://docs.docker.com/engine/reference/commandline/build/)

