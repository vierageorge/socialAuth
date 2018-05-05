# socialAuth

In this repo I'll be placing the files needed to create a simple web app in which someone can Authenticate via username/password or using Google account.

First, install to local virtual environment the following package `pip install social-auth-app-django`
After that, add to `settings.py`:
* INSTALLED_APPS: **social_django** and **register.apps.RegisterConfig**
* TEMPLATES -> OPTIONS -> context_processors: **social_django.context_processors.backends** and **social_django.context_processors.login_redirect**
* AUTHENTICATION_BACKENDS: **social_core.backends.open_id.OpenIdAuth**, **social_core.backends.google.GoogleOpenId**, **social_core.backends.google.GoogleOAuth2**, **django.contrib.auth.backends.ModelBackend**.
Then, migrate the database with a `python manage.py migrate`
