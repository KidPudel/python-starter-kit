# Check if django is installed
```bash
python -m django --version
```
# Create an environment "project"
```bash
django-admin startproject mysite
```
This creates a project "mysite".
Project is just an environment, _we haven't actually created an application_ (views or logic of our app).  

**_So far this step created an environment where the application is going to be hosted_**.

```
projectname/
    manage.py
    projectname/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```

These files are:

- The outer `projectname/` root directory is a container for your project. Its name doesn’t matter to Django; you can rename it to anything you like.
- manage.py: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about `manage.py` in django-admin and `manage.py`.
- The inner `projectname/` directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. projectname.urls).
- `projectname/__init__.py`: An empty file that tells Python that this directory should be considered a Python package.
- `projectname/settings.py`: `Settings/configuration` for this Django project. Django settings will tell you all about how settings work.
- `projectname/urls.py`: The URL declarations for this Django project; a “table of contents” of your Django-powered site.
- `projectname/asgi.py`: An entry-point for ASGI-compatible web servers to serve your project.
- `projectname/wsgi.py`: An entry-point for WSGI-compatible web servers to serve your project.

# Run the project
```bash
python manager.py runserver
```
also, probably you would need to migrate
```bash
python manager.py migrate
```
that would fix the issues of "unapplied migrations"


## But wait, what is actually the difference between project and application?

_An **app is a web application that does something** – e.g., a blog system, a database of public records or a small poll app_. _A **project is a collection of configuration and apps** for a particular website_. A project can contain multiple apps. An app can be in multiple projects.  



# Create an application
now that we have our environment setted up, it's time to actually create an application
```bash
python manager.py startapp myapp
```

this will generate `myapp` application with the following structure:   
```bash
myapp/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```

# Create your first view
