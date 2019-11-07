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
</br>

> - [Java JDK](https://www.oracle.com/technetwork/pt/java/javase/overview/index.html) - Java Development Kit (min version 8)
> - [Maven](https://maven.apache.org/) - Dependency management (mim version 3.3)
> - [Mysql](https://www.mysql.com/) - Database
> - [Docker](https://www.docker.com/) - Infrastructure settings
> - [Docker-compose](https://docs.docker.com/compose/) - Container orchestrator
> - [Firebase](DEVELOPERS.md)

</br></br>

## Environment variables:
Set the following variables for the project:
</br>

 > ##### JWT_SECRET = {jwt_secret} </br>
 > ##### DB_URL = jdbc:mysql://{ip}:{port}/{db_schema} </br>
 > ##### DB_USER = {username} </br>
 > ##### DB_PASSWORD = {password} </br>
 > ##### MAIL_HOST = {mail_host} </br>
 > ##### MAIL_PORT = {mail_port} </br>
 > ##### MAIL_USER = {mail_user} </br>
 > ##### MAIL_PASSWORD = {mail_password} </br>

</br></br></br>

Where {ip}, {port}, {db_schema}, {username}, {password}, {mail_host}, {mail_port}, {mail_user} and
{mail_password} must be replaced with actual database and mail values.
