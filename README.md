django_skl
==========

A modern Django (1.7) project skeleton.

![A fancy Django project skeleton](https://github.com/immensa/django_skl/raw/master/project_name/media/skel.jpg)


Install
=======

django_skl currently supports Django 1.7. To create a new django_skel base
project, run the following command (this assumes you have Django 1._ installed
already):

    $ django-admin.py startproject --template=https://github.com/immensa/django_skl/zipball/master name_project_cool
    $ heroku config:add DJANGO_SETTINGS_MODULE=name_project_cool.settings.prod


Where ``name_project_cool`` is the name of the project you'd like to create.

This is possible because Django 1.7's ``startproject`` command allows you to
fetch a project template over HTTP (which is what we're doing here).

While not strictly required, it is also recommended to do

     $ heroku config:add SECRET_KEY=putsomethingfairlycomplexhere

The production settings pull SECRET_KEY from environment but fallbacks
to a value which is generated mainly for development environment.

This setup allows you to easily keep your site in a public repo if you so 
wish without causing opening a route to attack your Django passwords.

Based
=====

https://github.com/rdegges/django-skel