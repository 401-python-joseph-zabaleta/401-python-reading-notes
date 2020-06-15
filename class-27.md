# Reading Notes 27 

## Articles  

### Using Models  
* [Link to Article](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)  
  
Django web applications access and manage data through Python Objects referred to as models. Before you coding a model, take time to consider the data that needs to be stored and the relationships between the different objects.  

#### Model Primer  
- Models are usually defined in an applications model.py file.  
- They are implemented as subclasses of `django.db.models.Model`  
- They can include: fields, methods, and metadata.  

##### Fields  
- A model can have an arbitrary number of fields  
- Each one will represent a column of data that we want to store in one our database tables.  
- Field name is used to refer to in queries and templates.  
- Common Field Arguments:  
    - `help_text`  
    - `verbose_name`  
    - `default`  
    - `null`  
    - `blank`  
    - `choices`  
    - `primary_key`  
- Common Field Types:  
    - `CharField`  
    - `TextField`  
    - `IntegerField`  
    - `DataField` and `DateTimeField`  
    - `EmailField`  
    - `FileField` and `ImageField`  
    - `AutoField`  
    - `ForeignKey`  
    - `ManyToManyField`  

##### MetaData
- Can control the default ordering of records returned when you query the model type.  
- Allows you to create and apply new "access permissions" for the model.  
- Allows ordering based on another field.  
- Declare a class is abstract.  

##### Methods  
- A model can also have methods.  
- Common method to include is `get_absolute_url()`  


### Django Admin
* [Link to Article](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)  
NOTE: The tutorial is really good but some of the tools are dated so when reading try to understand the concepts more than the code. 

- Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records.
- You must register your models in the admin.py  
- Creating superusers, using manage.py createsuperuser this will prompt user input and email and password



## Additional Resources  
* [Beginner's Guide to Django - Part 1](https://simpleisbetterthancomplex.com/series/2017/09/04/a-complete-beginners-guide-to-django-part-1.html)  

## Bookmark/Skim  
* [Beginner's Guide to Django - Part 2](https://simpleisbetterthancomplex.com/series/2017/09/11/a-complete-beginners-guide-to-django-part-2.html)  