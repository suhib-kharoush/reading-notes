# Linux Containers:
- Docker is really just Linux containers which are a type of virtualization.

- Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm.


#### Containers vs Virtual Environments:
- Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

#### Install Docker:
- To install Docker we need to download the desktop app on our computer and create a free account.

- $ docker --version
Docker version 19.03.5, build 633a0ea

- sudo pip install docker-compose

- $ docker-compose --version
docker-compose version 1.24.1, build 4667896b

- To confirm Docker installed correctly we can run our first command docker run hello-world.

#### Images and Containers:
- Images and containers are the two fundamental concepts to grasp when you start with Docker.


# Library Website and API

- Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.