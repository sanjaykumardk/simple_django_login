# Simple Django Login Application

This is a simple Django application that provides basic user authentication features, including user registration, login, and logout.

## Features

- User Registration
- User Login
- User Logout
- User Authentication

## Prerequisites

- Python 3.6+
- Django 4.2.13+

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
