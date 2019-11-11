# {{ project_name }}

Simple Django project template.

## Features
* Python 3.7
* Django 2.2.x
* Django Debug Toolbar
* Django Rest Framework 3.10.x
* Pipenv
* Custom user model
* Postgres Client

## Installation
```bash
PROJECT_NAME=payment_service

django-admin startproject \
  --extension py,md \
  --template=https://github.com/rcmontoy/django-project-template/archive/master.zip \
  ${PROJECT_NAME}

cd ${PROJECT_NAME}
pipenv install
```

## Local Development
```bash
pipenv shell
./manage.py makemigrations
./manage.py migrate
```

## Setup PostgreSQL
```sql
CREATE DATABASE {{ project_name }};
CREATE USER {{ project_name }} WITH PASSWORD 'password01*';
ALTER ROLE {{ project_name }} SET client_encoding TO 'utf8';
ALTER ROLE {{ project_name }} SET default_transaction_isolation TO 'read committed';
ALTER ROLE {{ project_name }} SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE {{ project_name }} TO {{ project_name }};
```

## Create Super User
```bash
pipenv shell
./manage.py createsuperuser
```