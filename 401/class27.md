# Readings: Django Models

## Model

![](https://djangobook.com/wp-content/uploads/Django_ORM_600.png)

A model is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Generally, each model maps to a single database table.

## The basics of Models

- Each model is a Python class that subclasses django.db.models.Model.
- Each attribute of the model represents a database field.
- With all of this, Django gives you an automatically-generated database-access AP

## Fields:

The most important part of a model – and the only required part of a model – is the list of database fields it defines. Fields are specified by class attributes.

## Feilds type:
- ```CharField``` is used to define short-to-mid sized fixed-length strings. 

- ``TextField`` is used for large arbitrary-length strings. 

- `IntegerField` is a field for storing integer (whole number) values, and for validating entered values as integers in forms.

- `DateField` and DateTimeField are used for storing/representing dates and date/time information.

- `EmailField` is used to store and validate email addresses.

- `FileField` and ImageField are used to upload files and images respectively.

- `AutoField` is a special type of IntegerField that automatically increments. 

- `ForeignKey` is used to specify a one-to-many relationship to another database model 

- `ManyToManyField` is used to specify a many-to-many relationship

## model example: 

from django.db import models

    class MyModelName(models.Model):
        """A typical class defining a model, derived from the Model class."""

        # Fields
        my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')

# Django admin site

he Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data.

![](https://camo.githubusercontent.com/368745aa3203131e99dda2fe5835fd455af7859c9fd0308ca59c8e075ba990b0/68747470733a2f2f7261772e6769746875622e636f6d2f616c6573646f74696f2f646a616e676f2d61646d696e2d73686f7274637574732f67682d70616765732f696d616765732f646a616e676f2d61646d696e2d73686f7274637574732e706e67)


## Registering models :
on admin.py page :

    from .models import your_model

    admin.site.register(your_model)

## Creating a superuser:

from terminal :

        python3 manage.py createsuperuser

## Logging in and using the site

- To login to the site, open the /admin URL (e.g. http://127.0.0.1:8000/admin 
and enter your name and password that you used them to register as a superuser.

- to add data to the model click add and fill the fields 

- to save the data in the database click save 

## changing the default names of the new data object:

to change the default name use __str__ majic method in the model to return different value 

