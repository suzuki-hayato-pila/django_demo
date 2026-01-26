# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Django 5.2.9 project for a private diary application. The project is in early development stage with foundational configuration complete.

## Development Commands

```bash
# Activate virtual environment (Windows)
.venv\Scripts\activate

# Run development server
python manage.py runserver

# Database migrations
python manage.py makemigrations
python manage.py migrate

# Create superuser for admin access
python manage.py createsuperuser

# Django shell
python manage.py shell

# Create a new Django app
python manage.py startapp <app_name>
```

## Architecture

- **config/**: Django project configuration package
  - `settings.py`: Main settings with PostgreSQL database configuration
  - `urls.py`: URL routing (currently only admin configured)
  - `wsgi.py` / `asgi.py`: Web server gateway interfaces

- **Database**: PostgreSQL (`private_diary` database on localhost:5432)
  - Fallback SQLite available at `db.sqlite3`

- **Logging**: Console-based logging configured for Django and future `diary` app

## Dependencies

- Django 5.2.9
- psycopg2-binary 2.9.11 (PostgreSQL adapter)

## Notes

- No custom apps created yet - project is ready for app development
- Development mode (DEBUG=True) - not configured for production
- Logging is set up with DEBUG level for the `diary` app (anticipated future app)
