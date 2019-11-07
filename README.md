<img height=170 width=235 align="left" src="https://github.com/leroy-merlin-br/jobs/blob/master/logo.png">

#h1 lm-instala-parameters

Microservice of the [Leroy Merlin](https://www.leroymerlin.com.br/) installs project for definition of parameters.

# What is this repository for

The **Lm-Instala-Base** is meant to be a template for new LmInstala modules.

# Requirements

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
