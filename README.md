# {{ project_name }}

Simple Django project template.

## Features
* Django 2.2
* Python 3.7
* Pipenv
* Custom user model
* Django debug toolbar

## Installation
```shell
PROJECT_NAME=payment_service

django-admin startproject \
  --extension py,md \
  --template /Users/ryanmontoya/repos/django-project-template \
  $PROJECT_NAME


cd $PROJECT_NAME
pipenv install
pipenv shell
./manage.py makemigrations
./manage.py migrate
```
