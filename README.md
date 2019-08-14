# {{ project_name }}

Simple Django project template.

## Features
* Python 3.7
* Django 2.2.4
* Django Debug Toolbar
* Django Rest Framework 3.10.2
* Pipenv
* Custom user model

## Installation
```shell
PROJECT_NAME=payment_service

django-admin startproject \
  --extension py,md \
  --template=https://github.com/rcmontoy/django-project-template/archive/master.zip \
  $PROJECT_NAME


cd $PROJECT_NAME
pipenv install
pipenv shell
./manage.py makemigrations
./manage.py migrate
```
