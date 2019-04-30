# django-mymdb
Movie Database Application

### Install the requirements 
clone this repo and create a virtual environment

```
$ git clone https://github.com/blessedsibanda/django-mymdb.git
```
```
$ cd django-mymdb
```

```
$ virtualenv venv
```

activate the virtual environment
```
$ source venv/bin/activate
```

install the requirements
```
(venv) $ pip install -r requirements.dev.txt
```

### Create a postgres database
For linux ubuntu, run the following commands in the terminal  

(Make sure postgres server is installed in your system)

```
(venv) $ sudo -u postgres psql
```

```
postgres=# create database mymdb;
```

```
postgres=# create user mymdb_user;
```

```
postgres=# grant all on database mymdb to 'mymdb_user';
```

```
postgres=# alter user mymdb_user password 'pass123';
```

```
postgres=# alter user mymdb createdb;
```


exit the postgres shell

```
postgres=# \q
```

### Run migrations and create a super user
```
(venv) $ python manage.py makemigrations
(venv) $ python manage.py migrate
(venv) $ python manage.py createsuperuser
```
Finally, run the dev server
```
(venv) $ python manage.py runserver
```
