# Cinema-API

API service for cinema management written on Django Rest Framework 

### Features

- JWT authenticated
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors and image
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions

## Installing using Github

Install PostgreSQL and create db for project. Then run:

```shell
git clone https://github.com/luxuriant777/cinema-api-drf.git
cd cinema-api-drf 
python -m venv venv
source venv/bin/activate (Linux and macOS) or venv\Scripts\activate (Windows)
pip install -r requirements.txt
```

Use .env file for environment variables or set environment variables through command line.

Example:

```shell
set DB_HOST=<your db hostname>
set DB_NAME=<your db name>
set DB_USER=<your db username>
set DB_PASSWORD=<your db user password>
set DJANGO_SECRET_KEY=<your secret key>
```

Run migrations and run server:

```shell
python manage.py migrate
python manage.py runserver
```

### Getting access:
- create user via /api/user/register/
- get access token via /api/user/token/
- use access token in Authorization header for all other requests
- use refresh token in Authorization header for /api/user/token/refresh/ request

### Also you can run project in docker container:

Docker should be installed on your machine

```shell
docker-compose build
docker-compose up
```

docker-compose.yml contains default values for environment variables. You can change them in docker-compose.yml or in .env file

### Getting access via docker container
- Go to `127.0.0.1:8000/api/` and check project endpoints via DRF interface;
- You can create new admin user: enter container `docker exec -it <container_name> bash`, and create in from there;
- get access token via /api/user/token/
- use access token in Authorization header for all other requests
- use refresh token in Authorization header for /api/user/token/refresh/ request
