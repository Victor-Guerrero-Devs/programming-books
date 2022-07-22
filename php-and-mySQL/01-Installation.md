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
