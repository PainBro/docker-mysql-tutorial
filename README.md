# Docker MySQL Tutorial
A tutorial on how to create and use a mysql image through docker.

you can follow along with this tutorial or with the slideshow below.
--LINK TO SLIDESHOW--

## Prerequisites
For this tutorial it is assumed that you already have docker setup on your computer and know the basics of how to use it.

## Step 1 - Creating a MySQL Image
This step is farely simple. Once you have docker setup on your device, open your terminal and use the code below to create your image.

```
docker run --name [YOUR IMAGE NAME] -e MYSQL_ROOT_PASSWORD=[YOUR MYSQL PASSWORD] -d mysql:tag
```
