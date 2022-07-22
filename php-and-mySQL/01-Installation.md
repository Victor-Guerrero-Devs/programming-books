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
- directory must be empty for it to work (delete the sh file)
- alternatively, you can replace the above command with

```
git clone https://github.com/v-je/docker .
```

- let's look at some of these config files

  - `nginx.conf` = configures web server
  - `PHP.Dockerfile` = configures PHP extensions
  - `docker-compose.yml` = lists the programs that will be installed and executed when you start your server

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

- open your preferred web browser
- type `v.je` into the address bar and hit enter

### Adding an HTML file to it

- go to `websites/default/public` in your project directory
- make a file called `test.html`
- paste

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

- go to `v.je/test.html`
- you will see the new html file rendered by the browser

### Folder Levels

We have seen that three levels of directories: `websites/default/public`

This is so b/c the directory websites is meant to store multiple websites.

#### Create a new Website

1. make a directory called `mysite` within `websites`
2. make a directory called `public` within `mysite`
3. make a new file called `wow.html` within `websites/mysite/public`
4. insert some HTML boilerplate into `wow.html` and save it
5. type into the browser `mysite.v.je/wow.html`

Any directory within the `websites` directory is a sub-domain
of `v.je`

Certain files should not go within the `public` directory for security reasons

## Conclusion

- we set up a web server w/ Docker
- we hosted HTML files on it
- time to learn PHP
