# Readings: Intro to Django
![](https://www.infoshort.in/media/Books/django-app-development-1_jth5iyD.png)

## What is Django?
Django is a high-level Python web framework that enables rapid development of secure and maintainable websites. The Django web framework is a free, open source framework that can speed up development of a web application being built in the Python programming language.The Django web framework, deployed on a web server, can help developers quickly produce a web frontend that’s feature-rich, secure and scalable.

![](https://1.cms.s81c.com/sites/default/files/2019-09-04/django.png)

## The Structure of a Django Website:
A Django website consists of a single project that is split into separate apps. The idea is that each app handles a self-contained function that the site needs to perform. As an example, imagine an application like Instagram. There are several different functions that need to be performed:

- User management: Login, logout, register, and so on
- The image feed: Uploading, editing, and displaying images
- Private messaging: Private messages between users and notifications
## Django Model-View-Controller Pattern (MVC):
- Model defines the data structure. This is usually a database and is the base layer to an application.
- View displays some or all of the data to the user with HTML and CSS.
- Controller handles how the database and the view interact.

![](https://files.realpython.com/media/mvc_diagram_with_routes.e12c5b982ac8.png)
## Starting with Django :

1. Creating a project(WSL):

        django-admin startproject mysite
2. The development server(WSL):

        python manage.py runserver

3. Creating the app(WSL):

        python manage.py startapp app_name

4. Write your first view:

        from django.http import HttpResponse


        def index(request):
          return HttpResponse("Hello, world")
in the app_name file include the following code : 

        from django.urls import path
        from . import views

        urlpatterns = [
            path('', views.index, name='index'),
        ]
The next step is to point the root URLconf at the polls.urls module. In mysite/urls.py, add an import for django.urls.include and insert an include() in the urlpatterns list, so you have:

        from django.contrib import admin
        from django.urls import include, path

        urlpatterns = [
            path('app_name/', include('app_name.urls')),
            path('admin/', admin.site.urls),
        ]