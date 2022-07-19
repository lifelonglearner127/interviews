- [Explain Django Architecture](#explain-django-architecture)
- [Explain the django project directory structure?](#explain-the-django-project-directory-structure)
- [What are models in Django?](#what-are-models-in-django)
- [What are templates in Django or Django template language?](#what-are-templates-in-django-or-django-template-language)
- [What are views in Django?](#what-are-views-in-django)
- [What is Django ORM?](#what-is-django-orm)
- [What is the use of Middleware in Django?](#what-is-the-use-of-middleware-in-django)
- [What are Django Signals?](#what-are-django-signals)

### Explain Django Architecture
Django follows the MVT (Model View Template) pattern which is based on the Model View Controller architecture.
- The Model helps to handle database. It is a data access layer which handles the data.
- The Template is a presentation layer which handles User Interface part completely.
- The View is used to execute the business logic and interact with a model to carry data and renders a template.

Although Django follows MVC pattern but maintains its own conventions. So, control is handled by the framework itself.
Here, a user requests for a resource to the Django, Django works as a controller and check to the available resource in URL.
If URL maps, a view is called that interact with model and template, it renders a template.
Django responds back to the user and sends a template as a response.

### Explain the django project directory structure?

### What are models in Django?
A model in Django refers to a class that maps to a database table or database collection. Each attribute of the Django model class represents a database field.

### What are templates in Django or Django template language?
### What are views in Django?

### What is Django ORM?
Django ORM(Object Relational Mapper) enables us to interact with databases in a more pythonic way. It works as an abstraction layer between the models and the database. It is possible to retrieve, save, delete and perform other operations over the database without ever writing any SQL query.

### What is the use of Middleware in Django?
Middleware is a framework of hooks into Django’s request and response processing. It ls a light-weight, low-level plugin system for globally altering Django’s input or output. Each middleware component is responsible for doing some specific function. For example, Django includes a middleware component, AuthenticationMiddleware, that associates users with requests using sessions. 
During the request phase, before calling the view, Django applies middleware in the order it’s defined in Middleware, top-down. You can think of it as an onion. Each middleware class is a layer that wraps the view, which is in the core of the onion. If the request passes through all the layers of the onion, all the way to the view at the core, the response will then pass through every layer (in reverse order) on the way back out. 

### What are Django Signals?
Whenever there is a modification in a model, we may need to trigger some actions. 
Django provides an elegant way to handle these in the form of signals. The signals are the utilities that allow us to associate events with actions. We can implement these by developing a function that will run when a signal calls it.
