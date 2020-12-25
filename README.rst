=================
django-helloworld
=================



Установка
============

Предварительно необходимо установить нужные пакеты и зависимости:

::

  $ sudo apt update

::

  $ sudo apt install python3-dev python3-pip python3-virtualenv sqlitebrowser

::

    $ sudo pip install -r requirements.txt

После чего:

::

    $ python3 manage.py migrate

Увидим следующее:

::

    Operations to perform:
      Apply all migrations: admin, auth, contenttypes, sessions, sites
    Running migrations:

      Applying contenttypes.0001_initial... OK
      Applying auth.0001_initial... OK
      Applying admin.0001_initial... OK
      Applying admin.0002_logentry_remove_auto_add... OK
      Applying admin.0003_logentry_add_action_flag_choices... OK
      Applying contenttypes.0002_remove_content_type_name... OK
      Applying auth.0002_alter_permission_name_max_length... OK
      Applying auth.0003_alter_user_email_max_length... OK
      Applying auth.0004_alter_user_username_opts... OK
      Applying auth.0005_alter_user_last_login_null... OK
      Applying auth.0006_require_contenttypes_0002... OK
      Applying auth.0007_alter_validators_add_error_messages... OK
      Applying auth.0008_alter_user_username_max_length... OK
      Applying auth.0009_alter_user_last_name_max_length... OK
      Applying sessions.0001_initial... OK
      Applying sites.0001_initial... OK
      Applying sites.0002_alter_domain_unique... OK


Для доступа к админскому интерфейсу создадим суперюзера и пароль:

::

    $ python3 manage.py createsuperuser --username admin --email admin@mail.com

Увидим предложение создать пароль:

::

    Password:
    Password (again):

    Superuser created successfully.

Run application
===============

После чего можно запустить сервер::

    $ python3 manage.py runserver

теперь можно постучаться на  URL http://127.0.0.1:8000/ :

.. figure:: https://github.com/mfigura61/django/blob/main/docs/scr1.png
   :width: 315px
   :align: center
   :alt: A Django 'Hello World' program example


Также по той же ссылке можно получить доступ к админскому интерфейсу http://127.0.0.1:8000/admin :

.. figure:: https://github.com/mfigura61/django/blob/main/docs/scr2.png
   :width: 315px
   :align: center
   :alt: Django Admin Interface running

  
