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
├── manage.py
├── myapp/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── templates/
│   │   ├── registration/
│   │   │   ├── login.html
│   │   │   └── register.html
│   │   └── home.html
│   ├── tests.py
│   ├── urls.py
│   ├── views.py
│   └── forms.py
├── simple_django_login/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── requirements.txt
