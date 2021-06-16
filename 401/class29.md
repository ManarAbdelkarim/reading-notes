# Django Custom User

![](https://res.cloudinary.com/practicaldev/image/fetch/s--telQ4adK--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/8eavsyfs5juwq4pbj7m2.png)

sometimes we don't want to use only the feilds available in the built in user model or we want to change some feilds , for example we may want to make the user log in by using email instead of the username 

in today's read I will walk with you in the steps of how to create a custom user model

1. create an app and add it in the installed apps in the settings 

- let's call our new app "account"

    INSTALLED_APPS = [

        'account',
    ]
- then add AUTH_USER_MODEL

        AUTH_USER_MODEL = 'account.CustomUser' 

2. we will start bulding our custom model inside the app "account" model 

- import AbstractUser

        from django.contrib.auth.models import AbstractUser

- create a class "a model" and let's call it "Account", then fill it with the fields you want

        class CustomUser(AbstractUser):
        pass
        # add additional fields in here

3. create a new file in the accounts app called forms.py


        touch account/forms.py

4. We'll update it with the following code to largely subclass the existing forms.

        from django import forms
        from django.contrib.auth.forms import UserCreationForm, UserChangeForm
        from .models import CustomUser

        class CustomUserCreationForm(UserCreationForm):

            class Meta:
                model = CustomUser
                fields = ('username', 'email')

        class CustomUserChangeForm(UserChangeForm):

            class Meta:
                model = CustomUser
                fields = ('username', 'email')

5. Finally we update admin.py since the Admin is highly coupled to the default User model.

        # accounts/admin.py
        from django.contrib import admin
        from django.contrib.auth.admin import UserAdmin

        from .forms import CustomUserCreationForm, CustomUserChangeForm
        from .models import CustomUser

        class CustomUserAdmin(UserAdmin):
            add_form = CustomUserCreationForm
            form = CustomUserChangeForm
            model = CustomUser
            list_display = ['email', 'username',]

        admin.site.register(CustomUser, CustomUserAdmin)

