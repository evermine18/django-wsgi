# django-wsgi3

*django-wsgi3* is a fork of *django-wsgi2* that has been modified to be compatible with Django 4.2.


## Installation

This package can be installed from pip3:
```
pip3 install django-wsgi3
```

## Configuration

In the original [django-wsgi documentation](https://pythonhosted.org/django-wsgi/ "django-wsgi documentation") the configuration is based on modifying the *WSGI_APPLICATION* setting value in settings.py. This is enough for development purposes but does not work in a production environment. In a production environment, it is not clear the location of the WSGI application that the HTTP server has to target requests to. The documentation was vague about this point, so this package provides an alternative:

This is how django-wsgi2 is configured both for testing and production:

In your Django project wsgi.py file (project_root/project_name/wsgi.py), replace this line:
```python
from django.core.wsgi import get_wsgi_application
```
for this:
```pyton
from django_wsgi.handler import get_wsgi_application
```

That is all you need to do.

## Documentation

Additionanl documentation for django-wsgi2 can be found in the original django-wsgi package [documentation](https://pythonhosted.org/django-wsgi/).
