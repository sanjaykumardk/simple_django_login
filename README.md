# Simple Django Login Application

This is a simple Django application that provides basic user authentication features, including user registration, login, and logout.

## Features

- User Registration
- User Login
- User Logout
- User Authentication

## Prerequisites

- Python 3.x
- Django 3.x or later

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/simple-django-login.git
    cd simple-django-login
    ```

2. Create and activate a virtual environment:

    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Apply the database migrations:

    ```bash
    python manage.py migrate
    ```

5. Create a superuser (for accessing the Django admin):

    ```bash
    python manage.py createsuperuser
    ```

6. Run the development server:

    ```bash
    python manage.py runserver
    ```

7. Open your web browser and go to `http://127.0.0.1:8000` to see the application.

## Project Structure

```plaintext
simple-django-login/
├── db.sqlite3
├── manage.py
├── Practicals
│   ├── admin.py
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations
│   │   ├── 0001_initial.py
│   │   ├── __init__.py
│   │   └── __pycache__
│   │       ├── 0001_initial.cpython-311.pyc
│   │       └── __init__.cpython-311.pyc
│   ├── models.py
│   ├── __pycache__
│   │   ├── admin.cpython-311.pyc
│   │   ├── apps.cpython-311.pyc
│   │   ├── __init__.cpython-311.pyc
│   │   ├── models.cpython-311.pyc
│   │   ├── urls.cpython-311.pyc
│   │   └── views.cpython-311.pyc
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── SECE
│   ├── asgi.py
│   ├── __init__.py
│   ├── __pycache__
│   │   ├── __init__.cpython-311.pyc
│   │   ├── settings.cpython-311.pyc
│   │   ├── urls.cpython-311.pyc
│   │   └── wsgi.cpython-311.pyc
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── templates
    ├── index.html
    ├── login.html
    └── signup.html
```
Configuration
SECE/settings.py

Ensure you have the following in your settings:

python

INSTALLED_APPS = [
    ...
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'Practicals',  # Add your app here
]

MIDDLEWARE = [
    ...
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]

TEMPLATES = [
    {
        ...
        'OPTIONS': {
            'context_processors': [
                ...
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

URL Configuration
SECE/urls.py

python

from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('Practicals.urls')),  # Include app URLs
]

Practicals/urls.py

python

from django.urls import path
from . import views

urlpatterns = [
    path('', views.index_view, name='index'),
    path('register/', views.register_view, name='register'),
    path('login/', views.login_view, name='login'),
    path('logout/', views.logout_view, name='logout'),
    path('home/', views.home_view, name='home'),
]

Templates

    templates/index.html - Home page template.
    templates/login.html - Login page template.
    templates/signup.html - Registration page template.

Usage
User Registration

    Navigate to http://127.0.0.1:8000/register/
    Fill in the registration form and submit.

User Login

    Navigate to http://127.0.0.1:8000/login/
    Enter your credentials and submit.

User Logout

    Navigate to http://127.0.0.1:8000/logout/

Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request.
License

This project is licensed under the Creative Commons Zero Universal License, so edit and use to your heart's content! See the LICENSE file for details.
