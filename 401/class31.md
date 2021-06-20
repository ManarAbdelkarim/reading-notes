# Django REST Framework & Docker

## Docker overview

![](https://codereviewvideos.com/blog/wp-content/uploads/2017/08/docker-tutorial-825x510.jpg)

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. 

## The Docker platform
Docker provides the ability to package and run an application in a loosely isolated environment called a container. The isolation and security allow you to run many containers simultaneously on a given host. 

## Docker architecture

![](https://docs.docker.com/engine/images/architecture.svg)

## Docker objects

- Images

An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization.

- Containers

A container is a runnable instance of an image.

## Install Docker

1. install from https://www.docker.com/get-started
2. run command `sudo pip install docker-compose`

## Image Builds

run command `docker image build `

## Conclusion 

-Docker is a way to run Linux containers
- Containers are a lightweight alternative to Virtual Machines

- Dockerfile is a list of instructions for creating an image

- Images are made up of one or more layers

- Containers are a running instance of an image

- docker-compose.yml controls how to run the container

- Containers are stateless and ephemeral in nature. We can link - the local filesystem via volumes but things become more complex with databases (which we didn’t cover here).


# Library Website and API

![](https://ksr-ugc.imgix.net/assets/011/705/984/4ea78430d3ad7dc88106a7b973248ba7_original.jpg?ixlib=rb-4.0.2&crop=faces&w=1552&h=873&fit=crop&v=1463687041&auto=format&frame=1&q=92&s=16f9ae9168eecef976e5a19887afb152)

## Django REST framework

Django REST framework is a powerful and flexible toolkit for building Web APIs.

Some reasons you might want to use REST framework:

- The Web browsable API is a huge usability win for your developers.
- Authentication policies including packages for OAuth1a and OAuth2.
- Serialization that supports both ORM and non-ORM data sources.
- Customizable all the way down - just use regular function-based views if you don't need the more powerful features.
- Extensive documentation, and great community support.
- Used and trusted by internationally recognised companies - including Mozilla, Red Hat, Heroku, and Eventbrite.

## how Django REST Framework works

- Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django - Rest Framework; it always must be added to a project after Django itself has been installed and configured.

- The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

- To illustrate these concepts, we will build out a basic Library website with traditional Django and then extend it into a web API with Django REST Framework.

