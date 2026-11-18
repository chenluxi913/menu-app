# Little Lemon Restaurant

A Django learning project for a restaurant website, based on the Little Lemon tutorial. It includes a homepage, an about page, a reservation form, a menu and individual menu-item pages. Menu items can be managed through Django admin.

## Requirements

- Python 3.9 or newer compatible with Django 4.2
- Django 4.2.30
- SQLite (included with standard Python installations)

## Run locally

From this directory (the one containing `manage.py`):

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py loaddata sample_menu
python manage.py createsuperuser
python manage.py runserver
```

On Windows, activate with `.venv\Scripts\activate` instead. Visit http://127.0.0.1:8000/ and log in to http://127.0.0.1:8000/admin/ using the account you created. The sample fixture contains menu items only.

## Project layout

- `littlelemon/`: project settings and URL configuration
- `restaurant/`: models, views, forms, routes, templates, static assets, migrations, and sample menu data
- `manage.py`: Django management commands
- `Menu items.docx`: original course reference

## Notes

This is a tutorial-based development project, not a production deployment configuration. The local SQLite database and admin accounts are deliberately excluded. `DEBUG` is enabled for local learning. Set `DJANGO_SECRET_KEY` to a stable secret if needed; without it the app generates a temporary key on each process start, which can invalidate sessions after a restart. Set up deployment settings separately before hosting. The tutorial contains course-provided content and assets; check their usage terms before publishing or reusing them.
