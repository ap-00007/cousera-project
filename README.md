# Little Lemon Restaurant

A Django web application for the Little Lemon restaurant brand. The project includes a landing page, about page, reservation form, and menu browsing experience for an Italian, Greek, and Turkish Mediterranean restaurant.

## Overview

This project is built with Django and uses SQLite as the default database. It consists of:

- a project-level configuration in `littlelemon/`
- an app named `restaurant/` containing the business logic, templates, models, and forms

## Features

- Home page with restaurant offer and restaurant highlights
- About page describing the restaurant story and ownership
- Reservation page with a booking form
- Menu page listing available items
- Individual menu item detail page for each menu item
- Persistent data storage for menu items and table bookings

## Project Structure

```text
.
├── littlelemon/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── restaurant/
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── migrations/
│   ├── models.py
│   ├── static/
│   ├── templates/
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── db.sqlite3
├── manage.py
├── README.md
└── .gitignore
```

## Models

The app defines the following main models:

- `Booking`: stores booking details including first name, last name, guest count, and comments
- `Menu`: stores menu item names, pricing, and short descriptions

## Routes

The main application routes include:

- `/` - home page
- `/about/` - about us
- `/book/` - reservation form
- `/menu/` - menu listing
- `/menu_item/<int:pk>/` - individual menu item page

## Getting Started

1. Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

2. Install Django:

```bash
pip install django
```

3. Apply database migrations:

```bash
python manage.py migrate
```

4. Run the development server:

```bash
python manage.py runserver
```

5. Open the app in your browser:

```text
http://127.0.0.1:8000/
```

## Notes

- The project uses Django's default SQLite database setup defined in `littlelemon/settings.py`.
- Static assets and HTML templates live under `restaurant/templates/` and `restaurant/static/`.
- The app can be expanded with authentication, admin management, or additional menu and reservation functionality.

