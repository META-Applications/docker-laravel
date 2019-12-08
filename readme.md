# Docker Laravel
A Dockerized environment for Laravel, featuring:
- PHP 7.2
- MySQL 5.7
- phpMyAdmin
- Composer


## Requirements
* [Docker](https://www.docker.com/)
* [Docker Compose](https://docs.docker.com/compose/)
* [Node.js](https://nodejs.org/)


## How to use
1. Copy the `Dockerfile`, `docker-compose.yml` and `.dockerignore` from this repo into any pre-existing Laravel project
2. Copy the settings from `.env.example` into your `.env` file.
3. That's it, you're good to go! See the [commands](#commands) section below.


## Commands
| Command | Description
|---|-
| `docker-compose up -d` | Start the containers.
| `docker-compose down` | Stop the containers.
| `docker exec -it app bash -c "sudo -u devuser /bin/bash"` | Login to the container in order to use _Composer_, _Artisan_, etc (the containers must be started for this to work).


## Help / FAQs
### I've started the containers, now what?
You can now [view the application](http://localhost:8000) or [manage the database](http://localhost:8080) (use the `MYSQL_USER` and `MYSQL_PASSWORD` settings from `docker-compose.yml` to login to phpMyAdmin).

### I get an error - "Forbidden You don't have permission to access this resource", what should I do?
This is likely caused because the `public` directory doesnt exist. _Is Laravel installed?_  
Update `APACHE_DOCUMENT_ROOT` in the `Dockerfile` if you want to use a different directory.


## Contributors
[Donny Burnside](http://www.donnyburnside.com/)