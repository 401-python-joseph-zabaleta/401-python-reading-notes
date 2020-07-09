# Reading Notes 44  

## Articles  

### Django SASS Processor  
* [Link to Article](https://github.com/jrief/django-sass-processor#introduction)  

A processor designed to compile SASS/SCSS files without having to manage third party services nor special IDE plugins  

Features:  
- Refer SASS/SCSS files directly from your sources, instead of referring a compiled CSS file, having to rely on another utility which creates them from SASS/SCSS files, hidden in your source tree.
- Use Django's settings.py for the configuration of paths, box sizes etc., instead of having another SCSS specific file (typically _variables.scss), to hold these.
- Extend your SASS functions by calling Python functions directly out of your Django project.
- View SCSS errors directly in the debug console of your Django's development server.
- django-sass-processor converts *.scss or *.sass files into *.css

### Installation 
`pip install libsass django-compressor django-sass-processor`  


### SASS Language Introduction  
* [Link to Article](https://sass-lang.com/guide)

SASS = Syntactically Awesome Stylesheets, which adds logic to your styling documents. 
Key Features are:  
- Inheritance through extend  
- While, For and Each Loops in CSS  
- Using Sass Libraries  
- You can create Partial files, to modularize your CSS.  


## Bookmark/Skim  
* [SMACSS Docs](http://smacss.com/)   