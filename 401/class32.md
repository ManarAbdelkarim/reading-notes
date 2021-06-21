# Permissions & Postgresql

adding permissions to your end points allows you to restrict what can be done on particular end points so for example
if I can restrict to being read-only or I can restrict it to being visible to people who have logged in so on

Authentication or identification by itself is not usually sufficient to gain access to information or code. For that, the entity requesting access must have authorization.

![](https://learnbatta.com/assets/images/django/permissions-in-Django-Rest-Framework.png)

## Object level permissions
REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

## API Reference:

- AllowAny

The `AllowAny` permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.


- IsAuthenticated

The `IsAuthenticated` permission class will deny permission to any unauthenticated user, and allow permission otherwise.



- IsAdminUser

The `IsAdminUser` permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.


- IsAuthenticatedOrReadOnly

The `IsAuthenticatedOrReadOnly` will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.

## DjangoModelPermissions

- This permission class ties into Django's standard `django.contrib.auth` model permissions. 

- This permission must only be applied to views that have a .queryset property or `get_queryset()` method. 

- Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.

a. `POST` requests require the user to have the add permission on the model.

b. `PUT` and PATCH requests require the user to have the change permission on the model.

c. `DELETE` requests require the user to have the delete permission on the model.

## DjangoObjectPermissions

- This permission class ties into Django's standard object permissions framework that allows per-object permissions on models. In order to use this permission class, you'll also need to add a permission backend that supports object-level permissions, such as django-guardian.

- As with `DjangoModelPermissions`, this permission must only be applied to views that have a `.queryset` property or `.get_queryset()` method. Authorization will only be granted if the user is authenticated and has the relevant per-object permissions and relevant model permissions assigned.

a. POST requests require the user to have the add permission on the model instance.

b. PUT and PATCH requests require the user to have the change permission on the model instance.

c. DELETE requests require the user to have the delete permission on the model instance.

## Custom permissions

To implement a custom permission, override BasePermission and implement either, or both, of the following methods:

- `.has_permission(self, request, view)`

- `.has_object_permission(self, request, view, obj)`