# SQLpad Tutorial
When reading this tutorial keep in mind this tutorial is for the creation and accessing of a new docker mysql container.

## Networking
In order to connect a docker cotainer to an external source, we need to make it able to connect. So in order to do that, we create a network. 
In the terminal, we can use the template below to create a network.

```
docker network create -d bridge [yourNetworkName]
```

Where [yourNetworkName] is the name of the network you wish to create.

This creates a docker accessable nework to connect your containers to other sources.

below is the code we will use for the example.

```
docker network create -d bridge mynet
```

In this example, you will see, the name we gave to our network was "mynet".


## Setting up SQLpad
Now that we have a network, we will need to have something to connect. 

### Creating the container
The first thing we will make is a sqlpad container using the template below in the terminal.

```
docker run -p [desiredPort] -e SQLPAD_ADMIN=[yourAdminEmail] -e SQLPAD_ADMIN_PASSWORD=[yourAdminPass] -d --name=[sqlpadContainerName] --network=[yourNetworkName] sqlpad/sqlpad:[desiredSQLpadversion]
```
Below will explain what each segment of this code does

- docker run - Tells the terminal that this is a docker command and that it should be run
- -p [desiredPort] - Tells docker what network port the container should be made on
- -e SQLPAD_ADMIN=[yourAdminEmail] - Sets up an admin email for sqlpad 
- -e SQLPAD_ADMIN_PASSWORD=[yourAdminPass] - Sets the password for the admin email
- -d --name=[sqlpadContainerName]  - Sets the name of your sqlpad container
- --network=[yourNetworkName] - Tells docker to connect the container to your network
- sqlpad/sqlpad:[desiredSQLpadversion] - tells docker that sqlpad is the type of container you want and which version

Below is the code we will be using for this example.

```
docker run -p 3000:3000 -e SQLPAD_ADMIN=admin@sql.pad -e SQLPAD_ADMIN_PASSWORD=adminpass -d --name=sqlpadSoFun --network=mynet sqlpad/sqlpad:master
```

now if we use ```docker ps``` in our terminal, it will pull up our containers and you should see something similar to this

```
CONTAINER ID   IMAGE                  COMMAND                CREATED         STATUS         PORTS                    NAMES
14587e65b327   sqlpad/sqlpad:master   "/docker-entrypoint"   4 minutes ago   Up 4 minutes   0.0.0.0:3000->3000/tcp   sqlpadSoFun
```

### Using the container
now that we have sqlpad running we can log in through our browser. 
The url will be ```http://localhost
