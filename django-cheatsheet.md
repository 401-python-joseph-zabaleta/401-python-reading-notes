git push -u origin master# DJANGO PROJECT SETUP

## Starting a project
1. Create a repo folder to contain your files.
    - CD into this folder.
2. Establish your virtual enviroment with Poetry
    - `poetry init -n`
3. Add required dependencies for your project
    - `poetry add Django`
    - `poetry add --dev black`
4. SHELL UP
    - `poetry shell` 
5. Create your Django Project:
    - `django-admin startproject ProjectNameHere`
    - NOTE: you can add a `.` to the end of this command to eliminate nested your project in a folder.  
6. CD into project folder it should contain `manage.py`  

## Starting a app
1. Creating an app:
    - `python manage.py startapp SomeAppName`  
    - NOTE: `./manage.py` is short for `python manage.py`  

## Running your Server
- `python manage.py runserver`  
- `./manage.py runserver`

## Migrate Data
- `python manage.py migrate`  

## Setting up a super user.
- `./manage.py createsuperuser`




## Project Folder items
1. Create these folders at the root:
    - templates
    - static

### Settings.py
1. Add any apps to the installed apps list:
    - `'blog.apps.BlogConfig'`
2. Ensure templates folder is added to Templates list/object:  
    - `'DIRS': [os.path.join(BASE_DIR, 'templates')],`
3. Link your static files, CSS, JS, Images:
    - Add this to the bottom of the file
    - `STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]`
### Urls.py
1. Ensure to import the include library:
    - `from django.urls import include, path`
2. Add URL patterns to link to your app url patterns:
    - `path('', include('blog.urls')),`

## App Folder Items

### admin.py
1. Import models
    - `from .models import Post`
2. Register your models with admin:  
    - `admin.site.register(Post)`

### apps.py
1. Ensure classes for apps exist

### models.py
1. import get user model:
    - `from django.contri.auth import get_user_model`
2. Create class for your models:
    - extend the class `models.Model`
    - example: `name = models.CharField(max_length=64)`
3. If adding users follow this style:
    - `author = models.ForeignKey(get_user_model(), on_delete=models.CASCADE)`

4. Add `__str__` to return something better than object.  

5. Make migrations, and migrate when you create / edit a model.
    - `./manage.py makemigrations`
    - `./manage.py migrate`

### tests.py



### urls.py (apps)
1. First create this file it does not come standard.
    -`urls.py`  
2. Copy and paste the format from project's folder url patterns.
3. import your views for use:
    - `from .views import HomePageView, PostDetailView`
4. Add your path, then your view, and assign a name:
    - `path('', HomePageView.as_view(), name='home'),`
    - `path('post_details/<int:pk>', PostDetailView.as_view(), name='post_details'),`

### views.py
1. import any generice views you might use:
    - `from django.views.generic import ListView, DetailView`
    - `ListView`, `DetailView`, `TemplateView`
2. import models you plan to use with your views:
    - `from .models import Post`
3. Create class that extends a particular view that you plan to use:
    - `class HomePageView(ListView):`
3. Your classes will have an attribute of template_name and also model:
    - `template_name = 'home.html'`
    - `model = Post`

## Customer User Model

### settings.py
1. Add the app to installed apps 
2. Add auth user model to the file
    - `AUTH_USER_MODEL = 'account.CustomUser'`

### App: models.py
1. import abstract user
    - `from django.contrib.auth.models import AbstractUser`
2. extend your customeruser class  
    - `class CustomUser(AbstractUser)`  
3. add your str method  
    - `def __str__(self)`
    - `return self.username`  

### App: Admin.py
1. import UserAdmin and get_user_model, import .forms and .models
    - `from django.contrib.auth import get_user_model`  
    - `from django.contrib.auth.admin import UserAdmin`  
    - `from .forms import CustomUserCreationForm, CustomUserChangeForm`  
    - `from .models import CustomUser`  
2. create a custom user admin class that extends UserAdmin
    - `class CustomUserAdmin(UserAdmin):`  
        - add_form: `CustomUserCreationForm`
        - form: `CustomUserChangeForm`
        - model: `CustomUser`
        - list_display: `['email', 'username']`
3. Register the model:
    - `admin.site.register(CustomUser, CustomUserAdmin)`  

### Make migrations now.
1. manage makemigrations app name
2. manage migrate

