# How to use Docker to Upload Files onto Github

## Table of Contents
* [Overview](#Overview)
* [Materials](#Materials)
* [Software](#Software)
* [What is Docker? Why use Docker?](#WhatisDocker?WhyuseDocker?)
* [How to use Docker?](#How-to-use-Docker?)
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

# What is Docker? Why use Docker?
Docker is an open-source software that is available to anyone on any operating system that gives the user the ability to make a container. A container is a directory that must be initalized where it can store and deploy files in different workspaces. 

# How to use Docker
Docker is a software program that allows the user to create containers. To create a container, a 'Dockerfile' must be made to give instructions on how to create an image and then the newly created image is built to make a container. There are also many available images that can be downloaded from Dockerhub which could also be built to make a image. An image can either be a computer programming development kit or an operating system which is responsible to creating the container. The image also gives the container some the same functionalies such as running commands in programming language or operating system that was used to make the container.<br> After creating a container, it becomes a new directory on your computer to store and upload files. <br>
<br>
Docker is different from Git and Github since its not a version control software, where files or applications are updated automatically in realtime. Docker can connect with other softwares such as Git and Github which are version control softwares. After making images, they can be saved and retrieved from your Dockerhub account and a container can be deleted instantly after the container's files is uploaded and stored somewhere else, and this can be advantageous as holding many applications on a local computer can take a lot of disk space. 

# Procedure
This is a guide how to upload files from a local computer directory to Docker. In this guide, a Docker Ubuntu container will be created <br>
1. Install Docker on your computer and open up Dockerhub (if you have it) <br>
2. Install Git, this allows your computer to use Git commands and upload files to Github <br>
3. Open up two tabs of Command Prompt, Powershell or the Terminal <br>
4. Change directory (cd) to the directory where you stored your application. Make sure the files are there. <br>
5. On the other terminal or command prompt tab, make a Docker container <br>
6. To make a container, an image can be pulled from Docker. Run the command: 
```
docker pull ubuntu
``` 
This pulls the ubuntu image from Docker's website. Docker's GUI, Dockerhub has many preset images that be pulled. <br>
<br>
7. To make a container, run the following command:
```
docker run -ti ubuntu bash
```
If successful, you should see a container id in the command prompt or terminal with a bunch of random numbers and letters. That signifies a new container was made. <br>
<br>
8. In the container, install the following:
    * 
    * 
    * apt install git - Install git on the container to use Git commands
    * apt install ssh - Install ssh to go to a secure shell
```
apt list
```
apt list shows the current packages installed. When making a new container, the package list and versions of each package is not to up to date.
```
apt update
```
Running the apt update command shows what packages can be downloaded or upgraded to the latest version
```
apt upgrade
```
apt upgrade updates the package list to their latest available versions
```
apt install git
```
Git is installed on the container to use Git commands
```
apt install ssh
```
ssh is now usable to enter other secure shells or servers <br>
<br>
9. Make a new Github repository in you Github account <br>
<br>
10. Run the following command in the next command prompt or terminal window: 
```
docker run -v "computerdirectory":/"----" --rm -ti ubuntu:latest bash
```
* "---" is the new name of the new folder that will be made in the Docker container
* This commands links up the local host's current directory to the docker container. Files that are in the the local host computer appear in the container and       files in the container now shows up in the local host directory
11. In the container, run the following steps to upload your files to Github:
```
git init
```
```
git config --global user.name ""
```

```
git config --global user.email ""
```
    
```
git config --global remote.origin.url "Github Repo"
```

```
git config --list
```

```
git remote add origin
```

```
git branch
```

```
git checkout main
```

```
git pull origin main 
```
If an error occurs use the git pull command, use the following instead:
```
git pull origin main --allow-unrelated-histories
```

```
git push origin main
```
