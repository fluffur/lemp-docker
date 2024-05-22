# LEMP Stack Project with Docker

This project is a template for running a LEMP stack (Linux, Nginx, MySQL, PHP) using Docker.

## Project Structure

The project includes the following main components:

- **Nginx**: Web server for handling requests and serving static files.
- **MySQL**: Database management system for data storage.
- **PHP**: Programming language for server-side logic.

## Getting Started

To get started with the project, you will need Docker and Docker Compose installed.

### Installing Docker Desktop

You can find Docker Desktop installation instructions [here](https://docs.docker.com/desktop/).

## 

## Running the Project

To run the project, follow these steps:
1. Сreate a .env file in the root directory with the following content:
```env
MYSQL_ROOT_PASSWORD=root_password
MYSQL_USER=username
MYSQL_PASSWORD=user_password
MYSQL_DATABASE=my_database
```
2. Navigate to the directory `docker/`:
```bash
cd docker
```
3. Start the containers in detached mode:
```bash
docker compose up -d
```

## Stopping the Project

To stop the project, run the following command: 
```bash
docker compose down
```


## Configuration

### Nginx 
The MySQL database configuration is set in the `.env` file . Here you can specify the database name, user, and password.
The Nginx configuration file is located at `docker/nginx/nginx.conf`. It's already preconfigured, so you do not have to worry about it. 

### MySQL
The MySQL database configuration is set in the `docker-compose.yml` file and environment variables are loaded from the `.env` file you created.

### PHP
The PHP-fpm container image is described in `docker/php/Dockerfile`

