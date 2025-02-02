# Django REST Swagger

[![Build Status](https://travis-ci.org/darkman66/django-rest-swagger.svg?branch=stable%2F0.3.django2)](https://travis-ci.org/darkman66/django-rest-swagger)
[![pypi-version]][pypi]
[![license-badge]][license]


# Purpose

Intention of this fork is to make `branch 0.3.x stable` to work with 
* Django 2.2
* Python 3.7+ 

Yeah, I know...old branch but maybe some of you same as me got stuck with old open api and can't easily upgrade. I hope i helped to some of you with this fork :)

# An API documentation generator for Swagger UI and Django REST Framework

This project is built on the [Django REST Framework Docs](https://github.com/marcgibbons/django-rest-framework-docs) and uses the lovely [Swagger from Wordnik](http://swagger.io) as an interface. This application introspectively generates documentation based on your Django REST Framework API code. Comments are generated in combination from code analysis and comment extraction. Here are some of the features that are documented:

* API title - taken from the class name
* Methods allowed
* Serializers & fields in use by a certain method
* Field default values, minimum, maximum, read-only and required attributes
* URL parameters (ie. /product/{id})
* Field `help_text` property is used to create the description from the serializer or model.

## Quick start

1. ```pip install django-rest-swagger```

2. Add `rest_framework_swagger` to your `INSTALLED_APPS` setting:

    ```python
        INSTALLED_APPS = (
            ...
            'rest_framework_swagger',
        )
    ```

3. Include the rest_framework_swagger URLs to a path of your choice

    ```python
    patterns = ('',
        ...
        url(r'^docs/', include('rest_framework_swagger.urls')),
    )
    ```

for more information, see the [documentation][docs].

## Requirements
* Python (2.7, 3.3, 3.4, 3.5)
* Django (1.8+)
* Django REST framework (3.8+)
* PyYAML (3.10+)

## Bugs & Contributions
Please report bugs by opening an issue

Contributions are welcome and are encouraged!

## Special Thanks
Thanks to [BNOTIONS](http://www.bnotions.com) for sponsoring initial development time.

Many thanks to Tom Christie & all the contributors who have developed [Django REST Framework](http://django-rest-framework.org/)

## Contributors
* Marc Gibbons (@marcgibbons)
* Geraldo Andrade (@quein)
* Vítek Pliska (@whit)
* Falk Schuetzenmeister (@postfalk)
* Lukas Hetzenecker (@lukas-hetzenecker)
* David Wolever (@wolever)
* Brian Moe (@bmoe)
* Ian Martin (@aztechian)
* @pzrq
* @jfelectron
* Warnar Boekkooi (@boekkooi)
* Darren Thompson (@WhiteDawn)
* Lukasz Balcerzak (@lukaszb)
* David Newgas (@davidn)
* Bozidar Benko (@bbenko)
* @pySilver


### Django REST Framework Docs contributors:

* Scott Mountenay (@scottmx81)
* @swistakm
* Peter Baumgartner (@ipmb)
* Marlon Bailey (@avinash240)


[build-status-badge]: https://travis-ci.org/marcgibbons/django-rest-swagger.svg?branch=master
[build-status]: https://travis-ci.org/marcgibbons/django-rest-swagger
[pypi-version]: https://img.shields.io/pypi/v/django-rest-swagger.svg
[pypi]: https://pypi.python.org/pypi/django-rest-swagger
[license-badge]: https://img.shields.io/pypi/l/django-rest-swagger.svg
[license]: https://pypi.python.org/pypi/django-rest-swagger/
[docs-badge]: https://readthedocs.io/projects/django-rest-swagger/badge/
[docs]: http://django-rest-swagger.readthedocs.io/
