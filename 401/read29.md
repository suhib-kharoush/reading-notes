# Django Best Practices: Custom User Model

- AbstractUser vs AbstractBaseUser:
- - There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work.

### Custom User Model:
- Creating our initial custom user model requires four steps:

- - update config/settings.py
- - create a new CustomUser model
- - create new UserCreation and UserChangeForm
- - update the admin

### Superuser:
- It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command line type the following command and go through the prompts.


### DjangoX:
- Django 3.1 & Python 3.8
- Install via Pip, Pipenv, or Docker
- User log in/out, sign up, password reset via django-allauth
- Static files configured with Whitenoise
- Styling with Bootstrap v4
- Debugging with django-debug-toolbar
- DRY forms with django-crispy-forms
![](https://github.com/wsvincent/djangox/raw/master/homepage.png)