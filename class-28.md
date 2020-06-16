# Reading Notes 28

## Articles  

### Django Forms 
* [Link to Article](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms)  

Django Admin site uses forms to present itself.  
- HTML Form is a group of one or more fields/widgets on a webpage.  
- Forms are a flexible mechanism for collecting user input and because there are suitable widgets for entering many different types of data, including text boxes, checboxes, radio buttons, data pickers and so on.  

Things Django Form handling does:  
- Display the default form the first time it is requested by the user.  
- Receive data from a submit request and bind it to the form.  
- Clean and validate the data.  
- If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.  
- If all data is valid, perform required actions.  
- Once all actions are complete, redirect the user to another page.  

- Django simplifies handling forms by providing programmatic mechanisms to declare, render, and validate forms.  
- Django provides generic form editing views that can do almost all the work to define pages that create, edit, and delete records associated with a single model.  

## Bookmark/Skim  
* [Django Templates](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Home_page)  
* [Django Views](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Generic_views)  