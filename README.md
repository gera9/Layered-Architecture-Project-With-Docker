# Layered-Architecture-Project-With-Docker
DAS Sistemas project.

Run this project by typing in your terminal `docker-compose up` or `docker-compose up -d` to hide the container logs.

Technologies we use:
  * Angular
  * Node.JS
  * MongoDB
  * Python
  * Docker

![mean](https://victorgraciaweb.com/wp-content/uploads/2017/10/meancover-0e4b0e4d-de65-4761-8641-e0ae3226fe3f.jpg)

How is it composed?

* The firt container runs MongoDB from the `mongo` image and use its respective volume to the data persistence.
* The second container runs a MongoDB DMBS: `mongo-express`. It's protected by using a basic authentication. Their credentials are:
  * User: foo
  * Password: bar123 
* The third container is named generator. This container inserts 1000 records to the `MongoDB` database obtained of a XML file. We use Python.
* The fourth container is an API. We use Node.JS and Express. We structure our project by using the software design pattern. It's divided mainly in three parts:
  * Controllers: 
  * Routes:
  * Models: 
* The fifth container runs Angular...
