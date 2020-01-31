django-23916
============

For demonstrating that https://github.com/django/django/pull/12313 works to fix the ticket.

```
python -m venv venv
source venv/bin/activate
pip install -e path/to/django
python manage.py makemigrations
python manage.py makemigrations
```

`makemigrations` will repeatedly generate new migration files for the `Author` model's case change (from `AuThor`) before the fix in that PR.
Afterwards, no migration files will be generated.
