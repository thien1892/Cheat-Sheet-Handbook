# Make venv
```bash
# Make folder in local computer
mkdir [LOCAL_FOLDER]
cd [LOCAL_FOLDER]

#Create venv
# pip3 install virtualenv
python3 -m venv [NAME_VENV]
source [NAME_VENV]/bin/activate

# install django
pip install django
# check:
python3 -m django version
# create a project
django-admin startproject [NAME_PROJECT]
# runserver - deploy django app
cd [NAME_PROJECT]
python3 manage.py runserver # to quit press ctrl + C
# Start an app
python3 -m django startapp myapp
```
# CML in Django
```bash
# migration
python manage.py makemigrations
python manage.py migrate
# Show migrations
python manage.py showmigrations
# Return version, example [VERSION] = 0002
python manage.py migrate [APP_NAME] [VERSION]
# Create super user
python manage.py createsuperuser
# Run app
python manage.py runserver
```

# Install mySQL in Ubuntu
```bash
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql.service
# sudo apt-get install python3-dev default-libmysqlclient-dev build-essential
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
flush privileges;
exit
# create database
mysql -u root -p # enter password
Create database mydatabase;
Show databases;
# install VS Code extension for MySQL
```

# Install MySQL in Django
```bash
#pipenv install django
pipenv install mysqlclient
mysql -u root -p # enter password
CREATE DATABASE reservations; # create database
SHOW DATABASES; # check database was created
CREATE USER 'admindjango'@'localhost' IDENTIFIED BY 'employee@123!';  # create new user
GRANT ALL ON *.* TO 'admindjango'@'localhost'; # grant permission
#Privileges assigned using GRANT command do not require the flush privileges but it is usually a good practice #to run this command while you are using variable commands for changing privileges and reloading the server #and grant tables containing information about user accounts. 
flush privileges;
exit;

##
mysql -u admindjango -p
use reservations;
show tables;
describe [TABLE_NAME];

```

# Configuring MySQL Connection
```bash
# Install MySQL DB API Driver
pip3 install mysqlclient
# Change in setting file
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'mydatabase',
        'USER': 'root',
        'PASSWORD': 'password',
        'HOST': '127.0.0.1',
        'PORT': '3306',
        'OPTIONS': {
            'init_command': "SET sql_mode='STRICT_TRANS_TABLES'"
        }
    }
}
# migrate
python manage.py migrate
```

# Use template and static
```bash
# in setting project
# Change 'DIRS': ['templates'] in TEMPLATES
# add STATICFILES_DIRS = ['static',]
cd ~/[PROJECT_NAME]
mkdir templates
mkdir static
# add template in folder templates
# add static: img, css in folder templates
# to use static in templates
# add {% load static %}
# "{% static 'myapp/img/logo.jpg' %}"

#use template:
# create templates layout.html {% block title %} {% endblock %}
# in another file html {% extends 'myapp/layout.html' %}
# {% block title %} ...{% endblock %}
```

# Django REST framework

## 1.[Different types of routing in DRF](https://www.coursera.org/learn/apis/supplement/cFRCv/different-types-of-routing-in-drf)
## 2.[Generic views and ViewSets in DRF](https://www.coursera.org/learn/apis/supplement/AlxEs/generic-views-and-viewsets-in-drf)
## 3. [ood routes versus bad routes](https://www.coursera.org/learn/apis/supplement/wRYeY/good-routes-versus-bad-routes)
