# Django

* Overview
  - High level web framework
  - MTV( Model-Template-View) Design Pattern
  - Opinionated
* Setup
  - Single project can have multiple apps
  - manage.py : CLI interface for the project
  - project-folder
    - settings.py : project settings
      - secret key
      - debug mode
      - domain names
      - installed apps
      - middlewares
      - templates
      - databases
    - urls.py : routing
    - wsgi.py : web server standard
    - migrations - DB schema migrations
  - app-folder
    - admin.py - add models to admin
    - apps.py - app sepcific settings
    - models.py - db models
    - tests.py - testcases
    - views.py - controller, methods
    - Create templates folder here
  - defualt is Jinja for templates
* Commands
  - Run server - `python manage.py runserver`
  - Create migrations file - `python manage.py makemigrations blog`
  - Migrate - `python manage.py migrate`
  - Create admin user - `python manage.py createsuperuser --username=alpha --email='abc@xyz.com'`
  - Create app `python manage.py startapp blog`
  - interactive shell `python manage.py shell`
* URL Patterns
  - specified with regexes
    - `url(r'^$', views.home, name='home')`
    - `url(r'^cat/([0-9]+)$', views.category, name='category'),`
* Admin
  - Dashboard
  - Registering models to get CRUD functionalities
* models
  - define tables - column, data type and properties
  - relationships (foreignkeys)
  - meta
  - \__str__
* ORM
  - if Posts is the model
    - `Posts.objects.all()`
    - `Posts.objects.get(id)`
  - filters
    - \__lt, \__lte, \__gt, \__gte
    - `Posts.objects.filter(rating__gt=10)`
    - __iexact for case insensitve match
    - __contains or __icontains for sub string
    - __isnull True/False
    - field__foreignfield `Posts.objects.filter(category__title='Tutorial')`
  - complex queries are done using Q
    - `Posts.objects.filter(Q(published=true) & Q(title__icontains='tutorial'))`
    - `Posts.objects.filter(Q(published=true) | Q(title__icontains='tutorial'))`
    - `Posts.objects.filter(~Q(title__icontains='tutorial')`
* Qs
  - blank=ture vs null=true in django models
    - null=true sets NULL value for the column in db
    - blank=true states whether the field is required in forms or not
    - for CharField and TextField the default is stored as '', for others it can be NULL


#### Links
* Crash course intro - https://www.youtube.com/watch?v=D6esTdOLXh4
* https://stackoverflow.com/questions/8609192/differentiate-null-true-blank-true-in-django
