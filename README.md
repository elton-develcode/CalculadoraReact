<img align="right" src="https://github.com/leroy-merlin-br/jobs/blob/master/logo.png">

# Lm-Instala-Parameters

Microservice in [Leroy Merlin](https://www.leroymerlin.com.br/) **Instala** for parameter definition project.

</br></br>

## What is this repository for
</br>

The **Lm-Instala-Parameters** is a microservice for setting system parameters that **Instala**, such as which service to integrate with other APIs, as well as some settings of the system itself and other modules.

</br></br>
## Requirements
Basic technologies needed for the project:
</br>

 - [Java JDK](https://www.oracle.com/technetwork/pt/java/javase/overview/index.html) - Java Development Kit (min version 8)
 - [Maven](https://maven.apache.org/) - Dependency management (mim version 3.3)
 - [Mysql](https://www.mysql.com/) - Database
 - [Docker](https://www.docker.com/) - Infrastructure settings
 - [Docker-compose](https://docs.docker.com/compose/) - Container orchestrator
 - [Firebase](https://firebase.google.com/?hl=pt-BR) - Database for mobile and web

</br></br>

## Environment variables:
Set the following variables for the project in _docker-compse.yml_:
</br></br>

#### JWT 
 
JSON Web Token (JWT) is an industry-standard RCT 7519 method for performing two-party authentication through a signed token that authenticates a web request. This token is a Base64 code that stores JSON objects with data that allows request authentication.</br>
Simple Example: JWT_SECRET = {jwt_secret} </br></br>
 
#### DB_URL
 
 Is the required JDBC String to connect to mysql database with java or the mysql workbench tool too.</br>
 Simple Example: DB_URL = jdbc:mysql://{ip}:{port}/{db_schema} </br></br>
 
 #### DB_USER
 
 Parameter required for database access authorization.</br>
 Simple Example: DB_USER = {username} </br></br>
 
 #### DB_PASSWORD
 
 Parameter required for database access authorization.</br>
 Simple Example: DB_PASSWORD = {password} </br></br>
 
 #### MAIL_HOST
 
 Parameter required for authorization to access the deploy platform.</br>
 Simple Example: MAIL_HOST = {mail_host} </br></br>
 
 #### MAIL_PORT
 
 Parameter required for authorization to access the deploy platform.</br>
 Simple Example: MAIL_PORT = {mail_port} </br></br>
 
 #### MAIL_USER
 
 Parameter required for authorization to access the deploy platform.</br>
 Simple Example: MAIL_USER = {mail_user} </br></br>
 
 #### MAIL_PASSWORD
 
 Parameter required for authorization to access the deploy platform.</br>
 Simple Example: MAIL_PASSWORD = {mail_password} </br></br>

Where {ip}, {port}, {db_schema}, {username}, {password}, {mail_host}, {mail_port}, {mail_user} and
{mail_password} must be replaced with actual database and mail values.

Example for docker-compose.yml:
</br>
```
version: '3.1'
services:
  web:
    build:
      context: .
      dockerfile: Dockerfile
      args:
        PARAM: argument
    container_name: name_for_container_docker
    ports:
      - 8089:8080
    environment:
      DB_URL: jdbc:mysql://db_url:3306/database
      DB_USER: user
      DB_PASSWORD: password
      JWT_SECRET: token 
      MAIL_HOST: email@email.com
      MAIL_PORT: 123
      MAIL_USER: User
      MAIL_PASSWORD: password
      API_INSTALA: http://localhost:8086/lm-instala-api
      API_INSTALA_PDP: http://localhost:8087/lm-instala-provider
      API_INSTALA_AUTH: http://localhost:8086/lm-instala-api
      API_INSTALA_PARAM: http://localhost:8089/lm-instala-parameters
      API_INSTALA_I18N: http://localhost:8086/lm-instala-api
      API_INSTALA_SATSFTN: http://localhost:8086/lm-instala-rating
      API_KEY: key
```
 ###### Attention: _Important file identification_

</br></br>

### Running the project

1. Clone lm-install-parameters
> git clone url_parameters


2. On terminal type 
> mvn clean install -Dmaven.test.skip=true

3. After configuring docker-compose, on terminal at the root of the folder execute the command:
> docker-compose up --build

</br></br></br></br>

# Main Features
