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

## REST API

 After you sign up with Restcomm, you can find your Account SID and Auth Token by navigating to your profile → Account in the Restcomm Console.
 
 You then need to use these credentials in your request’s Authorization header using Basic authentication type (i.e. Authorization: Basic <base64-encoded AccountSID:AuthToken>)
 
 REST API can be tested using get accounts request

```bash
curl -X GET https://www.restcomm.com/restcomm/2012-04-24/Accounts/ACCOUNT_SID.json  \
   -u 'YourAccountSid:YourAuthToken'
``` 
 
 example for
 ```
Account SID: ACae6e420f425248d6a26948c17a9e2acf
Auth Token: 94fe4b386b6f8127d0b1ccad6f7dc805 
``` 
  
 ```bash
 curl --location --request GET 'localhost:8080/restcomm/2012-04-24/Accounts/ACae6e420f425248d6a26948c17a9e2acf.json' \
 --header 'Authorization: Basic QUNhZTZlNDIwZjQyNTI0OGQ2YTI2OTQ4YzE3YTllMmFjZjo5NGZlNGIzODZiNmY4MTI3ZDBiMWNjYWQ2ZjdkYzgwNQ==' 
```
