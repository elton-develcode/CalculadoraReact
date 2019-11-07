<img width=40% align="left" src="https://github.com/leroy-merlin-br/jobs/blob/master/logo.png">
<img width=40% align="right" src="https://github.com/elton-develcode/images/blob/master/logos/develcode2.png">
</br></br></br></br></br></br></br></br></br></br></br></br></br></br>

# Lm-Instala-Parameters

Microservice in [Leroy Merlin](https://www.leroymerlin.com.br/) **Install** for Parameter Definition project developed by [Develcode Tecnologia](https://www.develcode.com.br/).
</br></br>

## What is this repository for
The **Lm-Instala-Parameters** is for configuring system parameters, such as which service integrates with other APIs.
</br></br>

## Requirements
- JDK 8
- Maven >=3.3.x
- Mysql
- docker
- docker-compose
- [Firebase json](DEVELOPERS.md)

Environment variables:

    JWT_SECRET = {jwt_secret}
	DB_URL = jdbc:mysql://{ip}:{port}/{db_schema} 
	DB_USER = {username}
	DB_PASSWORD = {password}
	MAIL_HOST = {mail_host}
	MAIL_PORT = {mail_port}
	MAIL_USER = {mail_user}
	MAIL_PASSWORD = {mail_password}

Where {ip}, {port}, {db_schema}, {username}, {password}, {mail_host}, {mail_port}, {mail_user} and
{mail_password} must be replaced with actual database and mail values.
