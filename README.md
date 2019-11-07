<img width=40% align="left" src="https://github.com/leroy-merlin-br/jobs/blob/master/logo.png">
<img width=40% align="right" src="https://github.com/elton-develcode/images/blob/master/logos/develcode2.png">
</br></br></br></br></br></br></br></br></br></br></br></br></br></br>

# Lm-Instala-Parameters

> Microservice in [Leroy Merlin](https://www.leroymerlin.com.br/) **Install** for parameter definition project developed by [Develcode Tecnologia](https://www.develcode.com.br/).

</br></br>

## What is this repository for
</br>

> The **Lm-Instala-Parameters** is for configuring system parameters, such as which service integrates with other APIs, as well as some settings of the system or module itself.

</br></br>
## Requirements
Basic technologies needed for the project:
</br></br>

> - [Java JDK](https://www.oracle.com/technetwork/pt/java/javase/overview/index.html) - Java Development Kit (min version 8)
> - [Maven](https://maven.apache.org/) - Dependency management (mim version 3.3)
> - [Mysql](https://www.mysql.com/) - Database
> - [Docker](https://www.docker.com/) - Infrastructure settings
> - [Docker-compose](https://docs.docker.com/compose/) - Container orchestrator
> - [Firebase](DEVELOPERS.md)

</br></br>

## Environment variables:
Set the following variables for the project:
</br></br>

 > JWT </br>
 
JSON Web Token (JWT) is an industry-standard RCT 7519 method for performing two-party authentication through a signed token that authenticates a web request. This token is a Base64 code that stores JSON objects with data that allows request authentication.
Simple Example: JWT_SECRET = {jwt_secret} </br></br>
 
 > DB_URL
 
 Is the required JDBC String to connect to mysql database with java or the mysql workbench tool.
 Simple Example: DB_URL = jdbc:mysql://{ip}:{port}/{db_schema} </br></br>
 
 > DB_USER
 
 Parameter required for database access authorization.
 Simple Example: DB_USER = {username} </br></br>
 
 > DB_PASSWORD
 
 Parameter required for database access authorization.
 Simple Example: DB_PASSWORD = {password} </br></br>
 
 MAIL_HOST = {mail_host} </br>
 MAIL_PORT = {mail_port} </br>
 MAIL_USER = {mail_user} </br>
 MAIL_PASSWORD = {mail_password} </br>

</br>

Where {ip}, {port}, {db_schema}, {username}, {password}, {mail_host}, {mail_port}, {mail_user} and
{mail_password} must be replaced with actual database and mail values.
