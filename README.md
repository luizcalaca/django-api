## Python + Django

### Commands

#### Configure the enviroment

```
python -m venv env
source env/bin/activate
pip install django
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
