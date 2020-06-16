# Reading Notes 29  

## Articles  

### Django Custom User Model  
* [Link to Article](https://learndjango.com/tutorials/django-custom-user-model)  

Django ships with a built-in User model. However, official Django documentation highly recommends usering a customer user model for new projects.  

There are two morern ways to created a customer user model in Django:  
- AbstractUser  
- AbstractBaseUser  

Both Cases we can subclass them to extend existing functionality howerever `AbstractBaseUser` reqires much, much more work. Just avoid this until you don't need a tutorial on Django.  

Creating a Customer User Model Requires 4 steps:  
- Update `settings.py`
- create a new `CustomerUser` model 
- create new `UserCreation` and `UserChangeForm`  
- update the admin  

Create Superuser: It is helpful to have a superuser to test out the login/logout of your UserModel  

After you create and implement a customer user model, you can easily and at anytime add additional fields to it.  

## Additional Resources  

### Videos  
* [Creating a Custom User Model](https://www.youtube.com/watch?v=eCeRC7E8Z7Y&t=59s)  
* [Abstract User, User Profile and Signals in Django](https://www.youtube.com/watch?v=EudKs1HPUfE)  

## Bookmark/Skim  
* [Substituting a custom User Model](https://docs.djangoproject.com/en/3.0/topics/auth/customizing/#auth-custom-user)  