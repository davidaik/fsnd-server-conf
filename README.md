## Information required for Udacity FSND Linux Server Configuration project

### IP Address
    13.126.144.201

### SSH Port
    2200

### URL
    http://catalog.flairsome.com


### Software installed

1. Git 2.17.1
2. Apache 2.4.29
3. Postgresql 10.8
4. Python 3.6 virtual environment at /home/ubuntu/venvs/venv
5. The following packages plus more are installed in the virtualenv.

###### :-
    Flask==1.0.3
    google-api-python-client==1.7.9
    google-auth==1.6.3
    google-auth-httplib2==0.0.3
    httplib2==0.12.3
    psycopg2==2.8.2
    SQLAlchemy==1.3.4


### Configurations

1. WSGI app located at /var/www/html/myapp.wsgi
2. Catalog project located at /var/www/html/catalog
3. The apache2 VirtualHost file /etc/apache2/sites-enabled/000-default.conf was updated to make the wsgi app work with the virtual env and the Catalog app. These lines were added:

    WSGIDaemonProcess myapp python-home=/home/ubuntu/venvs/venv
    WSGIProcessGroup myapp
    WSGIScriptAlias / /var/www/html/myapp.wsgi

### Third-party resources used

1. Amazon Lightsail
