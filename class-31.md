# Reading Notes 31  

## Articles  

### Beginner's Guide to Docker  
* [Link to Article](https://wsvincent.com/beginners-guide-to-docker/)   
Docker is a way to run Linux Containers  


Images and Containers are the two fundamental concepts to grasp when working with Dockers.  
- An image is a snapshot in time of what a project contains.  
- A container is a running instance of the image.  

Baking Analogy:  
- A `Dockerfile` is the recipe for a cake.  
- An image is a snapshot of the recipe at a given time  
- a `docker-compose.yml` says how to make the cake  
- And the container is the actual, baked cake.  

Key Notes:  
- Docker is a way to run Linux Containers  
- Containers are a lightweight alternative to Virtual Machines  
- `Dockerfile` is a list of instruction for creating an image  
- Images are made up of one or more layers  
- Containers are a running instance of an image  
- `docker-compose.yml` controls how to run the container  
- Continers are stateless and ephemeral in nature. We can link the local filesystem via `volumes` but things become more complex with databases.  


### Django for APIs - Library Website  
* [Link to Article](https://djangoforapis.com/library-website-and-api/)   
- Django REST Framework is added just like any other third-party app.  
- Make sure to add it to the url patterns.  
- Views.py is generic.ListAPIView  
- Refer to Article for Tutorial.  

## Bookmark/Skim  
* [Beginner's Guide to Django REST Framework](https://learndjango.com/tutorials/official-django-rest-framework-tutorial-beginners)  