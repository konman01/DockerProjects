# Getting started

### 1.2 What is Docker
Docker is a tool used to create containers. Container is standardized unit of software. A package of code and dependencies to run that code.

### 1.3 - Why Docker and Containers?

A conatiner is independent from other containers
Self Containing

### 1.5 - Virtual Machines Vs Docker Container
virtual Machine is heavy weight, there will be huge usage of resources, performace can be bad

### 1.6 - Getting out Hands Dirty

#### Dockerfile

// base Image
FROM node:14

// work directory
WORKDIR /app

// Copy pacjage.json to current path
COPY package.json .

// Run command to be executed
RUN npm install

// copy remaining files from local 
COPY . .

// expose port 300- to outside world
EXPOSE 3000

// cammand to start the server
CMD ["node", "app.mjs"]

#### Docker commands

docker build .
docker run -p 3000:3000 <image id>






