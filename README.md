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
* Start the postgresql server
* Create a database named blog
* Create a database user named blog

```$ sudo -u postgres psql```

```postgres=# CREATE DATABASE blog;```

```postgres=# CREATE USER blog;```

```postgres=# GRANT ALL ON DATABASE blog TO blog;```

```postgres=# ALTER USER blog PASSWORD '*****';```

```postgres=# ALTER USER blog CREATEDB;```

* connect to your database

```postgres=# \c blog;```

* install the ```pg_trgm``` extension (in order to use trigrams in PostgeSQL)

```blog=# CREATE EXTENSION pg_trgm;``` 

* now exit the postgresql shell

```blog=# \q```

* replace the database PASSWORD setting in settings.py with the password you entered

### Application Start

* Run database migrations

```(venv)$ python manage.py migrate```

* Create a superuser

```(venv)$ python manage.py createsuperuser```

* Finally, run the development server and visit http://localhost:8000/blog in your browser

```(venv)$ python manage.py runserver```
