# 0 why use docker

# 1install the docker
~~~
https://docs.docker.com/install/linux/docker-ce/ubuntu/
~~~

#### 2 use the basic syntax in docker to operate images and container

##### 在docker里面使用一些基本的语法去操作镜像和容器

Image is like a class and container is like a instance of a class
镜像类似于类，容器类似于类的实例

#### 2.1 get a image from remote repository

#### 从远端仓库获取一个镜像

~~~
sudo docker pull hello-world
~~~

list images that was downloaded to your machine

列出本地机器上的镜像文件

~~~
sudo docker image
~~~

#### 2.2 get a instance of image, called container

##### 从镜像获取一个实例，被称为容器

~~~
sudo docker run hello-world
~~~

to see what containers are instanciated

查看容器包含了哪些实例(运行中的镜像)

~~~
sudo docker container ls
~~~

#### 2.3 dive into the container to see what it is

##### 进入容器，看里面包含了什么

~~~
sudo docker exec -it container-id bash
~~~

#### 2.4  the relationship between image and container

##### 镜像与容器之间的关系

通过运行镜像启动容器。镜像是一个可执行的包，包含运行应用程序所需的所有内容——代码、运行周期、库、环境变量和配置文件。。

A container is launched by running an image. An image is an executable package that includes everything needed to run an application--the code, a runtime, libraries, environment variables, and configuration files.

一个容器是一个镜像实例运行的周期。

A container is a runtime instance of an image--what the image becomes in memory when executed (that is, an image with state, or a user process). You can see a list of your running containers with the command, docker ps, just as you would in Linux.