# How to use Docker to Upload Files onto Github

## Table of Contents
* [Overview](#Overview)
* [Materials](#Materials)
* [Software](#Software)
* [Procedure](#Procedure)

# Overview
Git is a popular version control software many people in the technology industry uses to create different repositories to store different files to showcase their work or projects. By installing Git on a computer and running Git commands through the command prompt or terminal or by using Git's GUI Github, people can upload their files into a repository. A similar way to uploading files through the terminal is by using a program called Docker and Dockerhub. 

# Materials
* Computer

# Software
* Command Prompt or Powershell (Windows only) <br>
* Terminal (Linux/MacOS only) <br>
* Docker <br>
* Dockerhub <br>
* Git <br>

# What is Docker? Why should we use it?
Docker is an open-source software that is available to anyone on any operating system that gives the user the ability to make a container. A container is a directory that must be initalized where it can store and deploy files in different workspaces. 

# How to use Docker
Docker is a software program that allows the user to create containers. To create a container, a 'Dockerfile' must be made to give instructions on how to create an image and then the newly created image is built to make a container. There are also many available images that can be downloaded from Dockerhub which could also be built to make a image. An image can either be a computer programming development kit or an operating system which is responsible to creating the container. The image also gives the container some the same functionalies such as running commands in programming language or operating system that was used to make the container.<br> After creating a container, it becomes a new directory on your computer to store and upload files. <br>
<br>
Docker is different from Git and Github since its not a version control software, where files or applications are updated automatically in realtime. Docker can connect with other softwares such as Git and Github which are version control softwares. After making images, they can be saved and retrieved from your Dockerhub account and a container can be deleted instantly after the container's files is uploaded and stored somewhere else, and this can be advantageous as holding many applications on a local computer can take a lot of disk space. 

# Procedure
This is a guide how to upload files from a local computer directory to Docker. In this guide, a Docker Ubuntu container will be created <br>
1. Install Docker on your computer
2. Open up Dockerhub (if you have it)
3. Open up two tabs of Command Prompt or the Terminal
4. Change directory (cd) to the directory where you stored your application. Make sure the files are there.
5. On the other terminal or command prompt tab, make a Docker container
6. To make a container, an image can be pulled from Docker. Run the command 'docker pull ubuntu'. This pulls the ubuntu image from Docker's website. Docker's GUI, Dockerhub has many preset images that be pulled.   
7. To make a container, run the command: docker exec -ti ubuntu bash
8. 
