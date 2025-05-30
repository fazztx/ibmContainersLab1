# Steps for Docker

1. Open Docker Desktop 

2. Have a Dockerfile readily available 

Example:
	# Specifies the base image...
	FROM node:9.4.0-alpine
	# Add the following files to the image...
	COPY app.js .
	COPY package.json .
	# Execute the following commands...
	RUN npm install &&\
    		apk update &&\
    		apk upgrade
	# Exposes the port...
	EXPOSE  8080
	# Runs the app.
	CMD node app.js

3. Build image

docker build . -t myimage:v1
		
		myimage = name & v1 = tag

4. To run container

docker run -dp 8080:8080 myimage:v1
curl.exe http://localhost:8080

5. To stop container

docker stop $(docker ps -q)

6. To check if it stopped

docker ps