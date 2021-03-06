# Layered-Architecture-Project-With-Docker
DAS Sistemas project using Docker and more...

![docker-compose](https://producthackers.com/wp-content/uploads/2020/11/Docker-composer.png)

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
  * Controllers: It's between the Routes file and the Models file. It manages the requests, connects to the database using the model and produces a response.
  * Routes: Contains the endpoints and delegates the request to the controller.
  * Models: Models the type of that we want to save in the database.
* The fifth container runs Angular. This container builds (for production) the angular project and then runs it with `Nginx` on the port 4200.


---

**The teams recording is below:**

[Teams recording](https://n9.cl/rhxkz)


---

**Diagram**

![diagram](Diagram.png)
