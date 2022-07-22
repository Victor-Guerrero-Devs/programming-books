# Installation

## Introduction

- you build a static site with HTML, CSS and maybe JS files
- you need to upload them to a webserver so people can access it via the internet
- PHP is for the web server
- allows you to write scripts to make your website dynamic, e.g. populating the website with up-to-date info from a database
- in other words, PHP works with the web server to generate dynamic websites
- therefore, PHP requires a database with which to work
- we will build this database w/ mySQL

## Your Own Web Server

- to test your own PHP/mySQL combo, you need your own web server that supports both
- instead of uploading the changes to your web host to see them, you can do this on your computer much like the live server extension
- therefore, a huge time saver during development

## Four Ways to Create a Web Server on your Computer

### 1: Manually Installing All the Software Components

- Install Apache, PHP, MySQL
- Configure them precisely
- Takes a lot of time, effort and skill
- Therefore, not for beginners

### 2: Pre-packaged Installations

- Many are available
- Allows you to install them in one go with pre-made configurations
- However, issues like OS compatiblity, resource hungry, out of date software, security flaws, etc
- like #1, not ideal

### 3: Virtual Servers

- these are web servers that exist on other computers
- can use software like VirtualBox to get into them
- virtual servers often have pre-configured settings for PHP and mySQL
- still heavy resource wise, especially with memory

### 4. Docker

- somewhat like #3
  - runs the server in its own "container"
- handles all the configuration
- easy on resources
- best option for modern PHP development

## Docker Installation for Linux

- open the terminal and type

```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

- Now that docker is installed, start it up by typing

```
sudo systemctl enable docker
sudo systemctl start docker
```

- add yourself to the docker group so won't need sudo to run Docker apps

```
sudo usermod -aG docker ${USER}
```

- logout and then back in to activate this (this is required everytime to you change user groups)
- make a directory in which your website will be stored
- navigate to this directory via the terminal

## Getting Started with Docker

- software needed is now installed
- terminal is in the above mentioned directory
- now to set up the enviornment

```
docker run --rm -v ${PWD}:/install vjedev/installer:latest
```

- config files will be downloaded and copied to the directory
- directory must be empty for it to work
- alternatively, you can replace the above command with

```
git clone https://github.com/v-je/docker .
```

- let's look at some of these config files

  - `nginx.conf` = configures web server
  - `PHP.Dockerfile` = configures PHP extensions
  - `docker-compose.yml` = lists the programs that will be installed and execute when you start your werver

- the enviornment we set up is NGINX not Apache

  - both do the same job (i.e. web server)
  - NGINX is optimized for modern web needs
  - therefore, Apache comes second to NGINX since it comes from an older time

- download docker into the directory and execute to start up the server

```
docker compose up
```

- for the first time doing this, it will take a couple of minutes
- hereafter, any subsequent docker apps will be prepared much faster
- you can stop the server with `CTRL + C`
  - or you can use `docker compose down`
- you can start it up again with `docker compose up -d`

## Connecting to the Server and Creating Your First File
