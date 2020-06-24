# Reading Notes 33 

## Articles  

### JSON Web Tokens  
* [Link to Article](https://jwt.io/introduction/)  

#### What is JSON Web Token?  
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.  

#### When should you use JSON Web Tokens?  
- Authorization  
- Information Exchange  

#### What is the JSON Web Token structure?  
In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:  
- Header  
- Payload  
- Signature  

#### How do JSON Web Tokens work?  
In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.

Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema.

### DRG JWT Authentication  
* [Link to Article](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)  

KEY NOTE:  Refresh Token  
At first glance the refresh token may look pointless, but in fact it is necessary to make sure the user still have the correct permissions. If your access token have a long expire time, it may take longer to update the information associated with the token. That’s because the authentication check is done by cryptographic means, instead of querying the database and verifying the data. So some information is sort of cached.

There is also a security aspect, in a sense that the refresh token only travel in the POST data. And the access token is sent via HTTP header, which may be logged along the way. So this also give a short window, should your access token be compromised.

## Additional Resources  
### Videos
* [JWT with DRF](https://www.youtube.com/watch?v=Fhcn2qx-4VQ)   

## Bookmark/Skim  
* [Django Migrations Primer](https://realpython.com/django-migrations-a-primer/)  