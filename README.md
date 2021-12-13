# Lift Wordpress with Docker

There is two docker-compose file ,
1) docker-compose-ssl.yml
2) docker-compose.yml

if you have ssl for yours website , you should use the second one else use the first file

## Secure connection with ssl and redirection with ngnix proxy , encrypt with cerbot and letencrypt.
  - install docker from https://docs.docker.com/get-docker/
  
Steps:
1) mkdir wordpress_ssl
2) cd ./wordpress_ssl
3) copy the file docker-compose-ssl.yml and change it to docker-compose.yml
4) copy the file default to folder
5) create .env file and fill it with yours credentials
6) docker-compose up

## Without ssl 
Steps:
1) mkdir wordpress
2) cd ./wordpress
3) copy the file docker-compose.yml
4) create .env file and fill it with yours credentials
5) docker-compose up


example for .env file

```
# our .env #

#DB env variables
MYSQL_ROOT_PASSWORD=root_password
MYSQL_USER=#RDS USER
MYSQL_PASSWORD=# RDS PASS
MYSQL_HOST=#RDS PATH
MYSQL_DB_NAME=#DB collection name.

#wordpress env variables

#swag env variables

SWAG_EMAIL=#mail
SWAG_URL=#dns url
SWAG_DNSPLUGIN=#dns provided service

#WP env variables
WORDPRESS_AUTH_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_SECURE_AUTH_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_LOGGED_IN_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_NONCE_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_AUTH_SALT=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_SECURE_AUTH_SALT=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_LOGGED_IN_SALT=xxxxxxxxxxxxxxxxxxxxxxxxxxx
WORDPRESS_NONCE_SALT=xxxxxxxxxxxxxxxxxxxxxxxxxxx
```
