Author: H. Ibrahimy


Readme file
—---------------------------


1. Pull required docker images
—---
docker pull sehi/nodeapi
docker pull mongo
docker pull mongo-express


2. Run docker images with the following commands
—---
docker run -d --network mongo-network -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=admin --name mongodb -p 27017:27017 mongo


docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=admin --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express


3. Run the VueJS app from Github repo
https://github.com/hibrahimy/pizzaProject.git






The application has three parts 
1. The MongoDB, which stores the data
2. The VueJS, which presents a front-end UI
3. The NodeAPI that acts as middleware