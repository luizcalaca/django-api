## Python + Django

### Commands

#### Configure the enviroment

```
python -m venv env
source env/bin/activate
pip install django
```

#### Seeds database

```
python3 manage.py seed_db
```

#### Automated tests with pytest

```
cd backend
pytest
```

#### Importants

```
django-admin startproject core .
django-admin startapp app
python3 manage.py runserver
```

```
python3 manage.py migrate
python3 manage.py makemigrations
python3 manage.py createsuperuser
```

```
python3 manage.py migrate --run-syncdb
python3 manage.py makemigrations <app_name>
```

```
pip freeze > requirements.txt
```

## Troubleshooting

```
Delete the rows related to your application from database:

DELETE FROM django_migrations WHERE app='<app_name>';
Delete your app's migration folder

Finally:

./manage.py makemigrations <app_name>

./manage.py migrate <app_name>
Done. Table created.
```

## HTTP requests

### Registration

```
http://127.0.0.1:8000/api/registration/ POST

{
    "username": "luiz.calaca2",
    "password1": "!@#$!@#$",
    "password2": "!@#$!@#$",
    "is_host": true
}
```

### Login

```
http://127.0.0.1:8000/api/login/ POST

{
    "username": "luiz.calaca2",
    "password": "!@#$!@#$"
}
```

### Bookings

```
http://127.0.0.1:8000/api/bookings/ GET

headers {Authorization: Token d93792c5asdfasdfe744c414e2707}
```

### Properties

```
http://127.0.0.1:8000/api/properties/2 GET

headers {Authorization: Token d93792c5asdfasdfe744c414e2707}
```
