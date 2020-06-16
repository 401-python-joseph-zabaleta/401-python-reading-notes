# DJANGO PROJECT SETUP

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
