# Containerization of a NodeJS App

## Step 1
First, let’s create a simple node.js(express) application. 
Now, let's try to run our app in the terminal,

#### npm init
#### npm install express
#### node index.js

Our app is running now, to check, go to http://localhost:5000

## Step 2

The next step is to create a Dockerfile.
Dockerfile — contains all the commands that are to be executed, to build an image.
We will always start from a base image, and build our own image with our app in it.
For the base image, we are going to use the official node image available in dockerhub. 
Dockerhub — where users can create their own private/public repositories to contain their images and also can access any open-source image.

## Step 3
Build the image using Dockerfile.

#### docker build -t node-app:latest .

## Step 4

Create an instance of the image (container).
We created the image, now let’s run our image.
#### docker run --name express-api -d -p 5000:5000 node-app:latest
