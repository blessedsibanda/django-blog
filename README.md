# django-blog
## A blog using django

## To run this project

* Clone this repo

```$ git clone https://github.com/blessedsibanda/django-blog.git```

* cd into the project folder

```$ cd django-blog```

* create a virtual env 

```$ python3 -m venv venv```

* activate the virtual env

```$ source venv/bin/activate```

* install the ```requirements```

```(venv)$ pip install -r requirements.txt```

### Setup postgresql database
* Install postgresql 
* create a database named blog
* create a database user named blog

```$ sudo -u postgres psql```

```postgres=# CREATE DATABASE blog;```

```postgres=# CREATE USER blog;```

```postgres=# GRANT ALL ON DATABASE blog TO blog;```

```postgres=# ALTER USER blog PASSWORD '*****';```

```postgres=# ALTER USER blog CREATEDB;```

* start your postgresql server
* replace the database PASSWORD setting in settings.py with the password you entered

### Application Start

* Run database migrations

```(venv)$ python manage.py migrate```

* Create a superuser

```(venv)$ python manage.py createsuperuser```

* Finally, run the development server and visit http://localhost:8000/blog in your browser

```(venv)$ python manage.py runserver```
