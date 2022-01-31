# Mysql
# Quick reference

-	**Maintained by**:  
	[MySql developer community](https://dev.mysql.com/)

-	**Where to get help**:  
	[Database Adminstrators (Stack Exchange)](https://dba.stackexchange.com/questions/tagged/docker+mysql)

Also see the ["Getting Help with Mysql" article on the Mysql Knowledge Base](https://dev.mysql.com/blog-archive/getting-help-in-mysql-shell/).


# Quick reference (cont.)

-	**Where to file issues**:  
	Issues can be filed on [https://github.com/deck-app/](https://github.com/deck-app/mysql/issues) "Docker compose" Component, or on [GitHub](https://github.com/deck-app/mysql/issues)

-	**Supported architectures**: ([more info](https://github.com/docker-library/mysql support only amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/mysql/),

# What is Mysql?

MySQL is the world's most popular open source database. With its proven performance, reliability and ease-of-use, MySQL has become the leading database choice for web-based applications, covering the entire range from personal projects and websites, via e-commerce and information services, all the way to high profile web properties including Facebook, Twitter, YouTube, Yahoo! and many more.

For more information and related downloads for MySQL Server and other MySQL products, please visit
www.mysql.com (https://www.mysql.com)

![logo](https://raw.githubusercontent.com/docker-library/docs/c408469abbac35ad1e4a50a6618836420eb9502e/mysql/logo.png)

# How to use this image

## Start a `mysql` server instance using DECK

Install MySql from the DECK marketplace and follow the instructions on the GUI

## MySQL command line client

The following command starts `mysql` command line client against your original `mysql` container, allowing you to execute SQL statements against your database instance:

```console
$ mysql -h mysql_hostname -u example-user -p
mysql [(none)]> SHOW DATABASES;
```

## From terminal with Docker
```console
$ git clone https://github.com/deck-app/mysql.git
$ cd mysql
$ docker-compose up -d

```
### Edit `.env` file to change any settings before installing like mysql user name, password etc.
```console
docker-compose up -d
```
### Modifying project settings
From the DECK app, go to stack list and click on `project's More > configure > Advanced configuration` Follow the instructions below and restart your stack from the GUI

### Rebuilding from terminal
You have to rebuild the docker image after you make any changes to the project configuration, use the snippet below to rebuild and restart the stack
```console
docker-compose stop && docker-compose up --build -d
```