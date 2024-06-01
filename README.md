# My Django Project

A project to learn about running Django for web development

---

[Django Tutorial](https://docs.djangoproject.com/en/5.0/intro/tutorial01/)

---

-Initialize a project - create the project level file structure
    - startproject <project name> <project root>
    - `$ django-admin startproject mysite .`
- Initialize an app - create the app level file structure
    - startapp <app name> <app folder (optional)>
    - `$ python manage.py startapp poll`
- Run the server
    - '$ python manage.py runserver
- Create a view for the app
    - In `views.py` define a function (or class method)
    - Views accept the request and any data from the url as input
    - Views expect an HttpResponse or an Exception to be returned
    - Views will pass a context to the template, which allows for the passing of python objects to the template as named arguments
    - Views can use `try/except/raise` for error handling and return appropriate HTTP response codes
- Templates define how a view is formatted
    - Templates *should* be places under the app directory structure, `app/templates/app/template_name.html
    - [Template Guide](https://docs.djangoproject.com/en/5.0/topics/templates/)
    - A note from the tutorial - the templates use incomplete HTML, [complete HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#anatomy_of_an_html_document) should be used outside the demo
- Create the apps URLconf in urls.py
    - Map a route to the function (view) created above
    - The route can also be used to set variables with data in the url
    - define `app_name` within the config to set the app namespace, this will help keep urls in the template more loosely coupled to app views
- Point the project level URLconf to route to the app URLconf when the URL matches
- `path()` - 4 arguments, route, view, kwargs, and name
- Models are python classes that tell django how to structure the database table's schema
- Define the models, update the database
    - `$ python manage.py makemigrations <appname>`
    - `$ python manage.py makemigrations`
- Create a superuser to interact with the admin portal
    - `python manage.py createsuperuser`
- Update the app to specify models that can be modified by the admin

---

# To Do / Read
- Use postgres for a backend
- [Dry Principle](https://docs.djangoproject.com/en/5.0/misc/design-philosophies/#dry)
- [csrf tokens](https://docs.djangoproject.com/en/5.0/ref/templates/builtins/#std-templatetag-csrf_token)
- [complete HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#anatomy_of_an_html_document)
- [Template Guide](https://docs.djangoproject.com/en/5.0/topics/templates/)
- Finish the tutorial [part 5](https://docs.djangoproject.com/en/5.0/intro/tutorial05/)
