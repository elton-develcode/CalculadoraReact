<img align="right" width="20%" src="https://github.com/elton-develcode/images/blob/master/logos/logo_instala_146x146.png">

</br>

## Lm-Instala-Parameters

Microservice in [Leroy Merlin](https://www.leroymerlin.com.br/) - **Instala** for parameter definition project.

</br></br>

## What is this repository for
</br>

The **Lm-Instala-Parameters** is a microservice for setting system parameters that **Instala**, such as which service to integrate with other APIs, as well as some settings of the system itself and other modules.

</br></br>
### Requirements

Basic technologies / hardware needed for the project:

* **Software**
  * [Java JDK](https://www.oracle.com/technetwork/pt/java/javase/overview/index.html) - Java Development Kit 8+
  * [Maven](https://maven.apache.org/) - Dependency management 3.3+
  * [Mysql](https://www.mysql.com/) - Database 8+
  * [Docker](https://docs.docker.com/install) - Infrastructure settings 17.06.0+ 
  * [Docker-compose](https://docs.docker.com/compose/install) - Container orchestrator 1.6.0+

* **Hardware**
  * Core i3 processor or better
  * 2Gb Ram (recommended min 4GB)
  * Internet Access (required for Github Login)
  

* **Accounts**
  * [Adeo Artifactory](https://adeo.jfrog.io) account with an API Key to access prebuild Docker images
  
 </br></br>

### Quick start

1. Login with Docker to the required Artifactory docker registries :

```sh
docker login adeo-docker-lmfr-api-release.jfrog.io
docker login adeo-docker-lmfr-api-dev.jfrog.io
```

> To login to Artifactory docker registries, you have to use you LDAP account as login and your API Key as password. If you don't already have an API Key, you can generate one [here](https://adeo.jfrog.io/adeo/webapp/).

2. Clone this repository and go to the demo folder:

```sh
git clone https://github.com/leroy-merlin-br/lm-instala-parameters.git

cd innersource-advisor/demo
```

3. Use docker-compose to start :

```
docker-compose pull && docker-compose up
```

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

</br></br></br>

# Main Features

</br>

 - Translation Configuration Parameters
 - Search parameters for internal modules
 - Search parameters for extern modules (APIs) 
 
 </br></br></br>
