# Docker MySQL Tutorial
A tutorial on how to create and use a mysql image through docker.

you can follow along with this tutorial or with the slideshow below.
--LINK TO SLIDESHOW--

## Prerequisites
For this tutorial it is assumed that you already have docker setup on 
your computer and know the basics of how to use it.

## Step 1 - Creating a MySQL Container
In this step we will go over how to pull a mysql image to docker and make 
a container from it.

### Making the Image

First, you will have to pull mysql to docker. You can do this py using 
the following code in your terminal.

```
docker pull mysql
```

This will create a mysql image to use in creating your container.

### Making the Container

Next, we have to setup the container This step is farely simple. Once you have docker setup on your device, 
open your terminal and use the code below to create your image.

```
docker run --name [your-container-name] -e MYSQL_ROOT_PASSWORD=[your mysql password] -d mysql:[tag]
```

Replace [your-container-name] with the desired name for your mysql container

Replace [your mysql password] with the desired mysql root password

And replace [tag] with the version of mysql you'd like to use. Below are the available versions 
you can use.  

- 8.0.29-oracle, 8.0-oracle, 8-oracle, oracle
- 8.0.29, 8.0, 8, latest, 8.0.29-debian, 8.0-debian, 8-debian, debian
- 5.7.38-oracle, 5.7-oracle, 5-oracle
- 5.7.38, 5.7, 5, 5.7.38-debian, 5.7-debian, 5-debian
- latest

For this example, we will be using the code below.

```
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=mysqlpass -d mysql:latest
```

## Step 2 - Opening your container
