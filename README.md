# Linux-Server-Configuration
### Full Stack Web Development NanoDegree
_______________________
## About
This is a project which deploys a web application(Item-Catelog) on a configured linux server

## Accessing the linux server
* Download ssh private key ```garder``` from this repository
* ssh linux server via private key and port 2200 ```ssh garder@54.180.135.195 -i garder -p 2200```

## Quick Start
* Access ```http://54.180.135.195.xip.io``` and start browsing the web application
* The instuctions of the web application is described in ```README.md``` in repository **Item-Catelog**

## Installed Packages
* Ubuntu
  * apache2
  * git
  * **libapache2-mod-wsgi-py3**(wsgi_mod for python3)
  * libpq-dev
  * postgresql
  * python3
  * python3-pip
  * python-dev
  * python-psycopg2
  * request
* python
  * certifi==2019.3.9
  * chardet==3.0.4
  * Click==7.0
  * Flask==1.0.2
  * get==2019.3.22
  * httplib2==0.12.1
  * idna==2.8
  * itsdangerous==1.1.0
  * Jinja2==2.10
  * MarkupSafe==1.1.1
  * oauth2client==4.1.3
  * post==2019.3.22
  * psycopg2==2.8.1
  * public==2019.3.22
  * pyasn1==0.4.5
  * pyasn1-modules==0.2.4
  * query-string==2019.3.22
  * request==2019.3.22
  * requests==2.21.0
  * rsa==4.0
  * six==1.12.0
  * SQLAlchemy==1.3.2
  * urllib3==1.24.1
  * Werkzeug==0.15.2
  
## Configuration Changes
1. Update all currently installed packages.
2. Change the SSH port from 22 to 2200. Make sure to configure the Lightsail firewall to allow it.
3. Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
4. Create a new user account named grader.
5. Give grader the permission to sudo.
6. Create an SSH key pair for grader using the ssh-keygen tool.
7. Configure the local timezone to UTC.
8. Install and configure Apache to serve a Python mod_wsgi application.
   * mod_wsgi configuration: ```/var/www/html/Item-Catelog/myapp.wsgi/```
   * apache2 configuration: ```/etc/apache2/sites-enabled/000-default.conf```
   
## Third-Party Resources
* StackOverflow posts
  * How to configure Apache to use virtualenv and python3
  
    https://stackoverflow.com/questions/27450998/run-mod-wsgi-with-virtualenv-or-python-with-version-different-that-system-defaul
  * Which package to install when using python3 with psql (No module named _psycopg)
  
    https://stackoverflow.com/questions/21158918/django-mod-wsgi-psycopg2-improperlyconfigured-error-loading-psycopg2-module
  * How to set secret key outside of the Flask app script
  
    https://stackoverflow.com/questions/35657821/the-session-is-unavailable-because-no-secret-key-was-set-set-the-secret-key-on/35657961 
  * How to save login status in Flask app
  
    https://stackoverflow.com/questions/35307676/check-login-status-flask
    
  * How to install virtualenvwrapper in Python3
  
    https://medium.com/@gitudaniel/installing-virtualenvwrapper-for-python3-ad3dfea7c717
  
* Tutorials
  * How to install mod_wsgi and configure Apache
  
    http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/
  * How to use Apache WSGI with Flask App
  
    https://www.bogotobogo.com/python/Flask/Python_Flask_HelloWorld_App_with_Apache_WSGI_Ubuntu14.php
    


## Licience
The content of this repository is licensed under [Apache2](https://www.apache.org/licenses/LICENSE-2.0) licience.

