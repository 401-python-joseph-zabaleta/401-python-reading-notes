# Reading Notes 32  

## Articles  

### DRF Permissions  
* [Link to Article](https://www.django-rest-framework.org/api-guide/permissions/)  
  
  
#### API Reference  
- Permissions allow requests to be granted or denied access.  
- Permissions in REST framework are always dfined as a list of permission classes  

* AllowAny:  
    - The `AllowAny` permission class will allow unrestricted access.  
* isAuthenticated:    
    - The `isAuthenticated` permission class will deny permission to any unauthenticated user, and allow permission otherwise.  
* isAdminUser:  
    - The `IsAdminUser` permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.  
* IsAuthenticatedOrReadOnly:  
    - The `IsAuthenticatedOrReadOnly` will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; `GET`, `HEAD` or `OPTIONS`.  
* DjangoModelPermissions:  
    - This permission class ties into Django's standard `django.contrib.auth` model permissions. This permission must only be applied to views that have a `.queryset` property set. Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.  
* DjangoModelPermissionsOrAnonReadOnly:  
    - Similar to `DjangoModelPermissions`, but also allows unauthenticated users to have read-only access to the API.  
* DjangoObjectPermissions:  
    - This permission class ties into Django's standard `object permissions framework` that allows per-object permissions on models. In order to use this permission class, you'll also need to add a permission backend that supports object-level permissions, such as `django-guardian`.
* Custom Permissions:  
    - To implement a custom permission, override `BasePermission` and implement either, or both, of the following methods:
        - `.has_permission(self, request, view)`  
        - `.has_object_permission(self, request, view, obj)`  
    - The methods should return `True` if the request should be granted access, and `False` otherwise.  


## Bookmark/Skim 
* [Classy Django REST](http://www.cdrf.co/)  
* [DRF Generic Views](https://www.django-rest-framework.org/api-guide/generic-views/)  