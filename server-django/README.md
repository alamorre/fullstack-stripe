# Django Server for Stripe

## Setup Django project

# Create a virtual environment to isolate our package dependencies locally

```
# Create the project directory

mkdir server-django
cd server-django

# Create a virtual environment to isolate our package dependencies locally

python3 -m venv env
source env/bin/activate # On Windows use `env\Scripts\activate`

# Install Django and Django REST framework into the virtual environment

pip install --upgrade pip
pip install django
pip install djangorestframework

# Set up a new project with a single application

django-admin startproject server .
django-admin startapp posts
```

Create the `.gitignore` file with the following:

```
env/
*.sqlite3
```

Create database and first user:

```
./manage.py migrate
./manage.py createsuperuser --email <YOUR_EMAIL> --username <YOUR_USERNAME>
```

## Setting up user auth

### Add the following installed apps

```
    'rest_framework',
    'rest_framework.authtoken',
    'posts',
```

### Add the following URLS in `server/urls.py`

```
    path('admin/', admin.site.urls),
    re_path('login', views.login),
    re_path('signup', views.signup),
```

### Add code for the following files

`serializers.py`, `views.py`, `request.rest` in that order
