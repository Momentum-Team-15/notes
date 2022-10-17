# Users in Django

For most models, you can make changes to them throughout development. The exception to this is `User`. Django has several built in `User` 
models, which you can customize. You need to decide which option you are going to use at the beginning of a project. A good breakdown of
the options can be found in this [article](https://simpleisbetterthancomplex.com/tutorial/2016/07/22/how-to-extend-django-user-model.html)
In class, we are going to choose option 4, inheriting from `AbstractUser`, which is [here](https://github.com/django/django/blob/0dd29209091280ccf34e07c9468746c396b7778e/django/contrib/auth/models.py#L334) in the source code.


## Registration with Django Registration Redux

You *can* build your own registration, mechanism for users to sign up and log in, but we are going to use a tool for that called Django
Registration Redux. The simplest way to incorporate this tool is to:
1. `pipenv install django-registration-redux`
2. Add 'registration' to installed apps at the top in settings.py.
3. Create a templates directory with a template called base.html. It needs to exist and contain this:  
```py
{% block content %}
{% endblock %}
```
4. Follow the directions for the "Simple" (one step) setup found [here](https://django-registration-redux.readthedocs.io/en/latest/simple-backend.html).
