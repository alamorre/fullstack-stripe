# Django Server for Stripe Blog

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
django-admin startapp users
django-admin startapp blog
```
