# Reading Notes 34  

## Articles  

### Django Settings Best Practices  
* [Link to Article](https://djangostars.com/blog/configuring-django-settings-best-practices/)  

#### Managing Django Settings: Issues

Key issues you might run into:
- Different environments  
- Sensitive Data  
- Sharing settings between team members  
- Django settings are a Python Code (no problem for us!)  

#### Setting Configuration: Different Approaches  
There is no built-in universal way to configure Django settings without hardcoding them. But `books`, `open-source` and `work projects` provide a lot of recommendations and approaches on how to do it best.

#### 12 Factors  
12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider.  

1. Codebase  
2. Dependencies  
3. Config  
4. Backing services  
5. Build, release, run  
6. Processes  
7. Port binding  
8. Concurrency  
9. Disposability  
10. Dev/prod parity  
11. Logs  
12. Admin processes  

#### Django Settings: Best Practices  
- Keep settings in enviroment vairables.  
- Write default values for production configuration (excluding secret keys and tokens).  
- Don't hardcode sensitive settings, and don't put them in VCS.  
- Split settings into groups: Django, third-party, project.  
- Follow naming conventions for custom (project) settings.  


### SSH Tutorial  
* [Link to Article](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)  

#### What is SSH?  
SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. 

#### How does SSH Work  
There are three different encryption technologies used by SSH:
- Symmetrical encryption  
    - Secret Key used for both encryption and decryption  
    - Often called shared key or shared secret  
- Asymmetrical encryption
    - Uses two seperate keys for encryption and decryption  
    - Known as public key and private key  
    - forms a public-private key pair.  
- Hashing.
    - Hash-based Message Authentication Codes (HMACs)  
    



## Bookmark/Skim
* [White Noise](http://whitenoise.evans.io/en/stable/)  
* [IaaS](https://en.wikipedia.org/wiki/Infrastructure_as_a_service)  
* [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service)  
* [CORS](https://en.m.wikipedia.org/wiki/Cross-origin_resource_sharing)  