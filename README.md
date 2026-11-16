# Banking management project secure project

A Django project with 5 models.

## Tech stack

- Python 3
- Django
- Database: SQLite

## Project structure

- `banking_mgt_project/`: project settings and root URLs
- `client_app/`: Django app
- Tests: `client_app/tests.py`

## Data model

| Model | App | Fields |
|---|---|---|
| `User` | `client_app` | username, email, password, is_active, is_admin, is_staff, is_superuser |
| `Address` | `client_app` | houseNumber, street, city, country, zipCode |
| `Client` | `client_app` | cin, name, familyName, phoneNumber, address |
| `Account` | `client_app` | accountNumber, balance, type, client |
| `Operation` | `client_app` | operationNumber, type, amount, date, account |

## URL routes

Declared in `urls.py`:

- `/blog/`

## How to run

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Then open `http://127.0.0.1:8000/`.

---

Author: [Chaouki Bayoudhi](https://github.com/ChaoukiBayoudhi)
