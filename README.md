# Cinema-API

API service for cinema management written on Django Rest Framework 

## Installing using Github

Install PostgreSQL and create db

```shell
git clone https://github.com/luxuriant777/cinema-api-drf.git
cd cinema-api-drf 
python -m venv venv
source venv/bin/activate (Linux and macOS) or venv\Scripts\activate (Windows)
pip install -r requirements.txt
set DB_HOST=<your db hostname>
set DB_NAME=<your db name>
set DB_USER=<your db username>
set DB_PASSWORD=<your db user password>
set SECRET_KEY=<your secret key>
python manage.py migrate
python manage.py runserver
```
### Run with docker

Docker should be installed

```shell
docker-compose build
docker-compose up
```

### Getting access via docker container
- Go to `127.0.0.1:8000/api/` and check project endpoints via DRF interface;
- You can create new admin user: enter container `docker exec -it <container_name> bash`, and create in from there;

### Getting access locally
- create user via /api/user/register/
- get access token via /api/user/token/

### Features

- JWT authenticated
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors and image
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions
