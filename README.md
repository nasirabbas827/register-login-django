# register_login_django  

A Django‑based web application that provides user registration, authentication, and a simple blockchain‑backed voting system. The project demonstrates how to structure a Django app, manage migrations, and integrate custom business logic (e.g., a lightweight blockchain) while keeping the codebase clean and maintainable.

---  

## Overview  

`register_login_django` is a starter project for building secure user‑centric applications. It includes:

* **User registration & login** – standard Django authentication with custom forms.  
* **Profile management** – extended user model (`Profile`) storing additional fields such as date of birth, address, and profile picture.  
* **Blockchain‑based voting** – a minimal blockchain implementation (`myapp/blockchain.py`) that records votes immutably.  
* **Admin interface** – ready‑to‑use Django admin for managing users, candidates, and elections.  

The repository is organized as a conventional Django project (`manage.py`) with a single reusable app (`myapp`). All database schema changes are captured in the migration files under `myapp/migrations/`.

---  

## Features  

| ✅ | Feature |
|---|---------|
| ✔️ | **Secure registration & login** – password hashing, CSRF protection, and built‑in Django auth. |
| ✔️ | **Extended user profile** – first/last name, DOB, address, profile picture, and email verification. |
| ✔️ | **Election & candidate models** – create elections, add candidates, and track results. |
| ✔️ | **Simple blockchain** – each vote is stored as a block, guaranteeing tamper‑evidence. |
| ✔️ | **Admin dashboard** – full CRUD for users, profiles, elections, and blockchain entries. |
| ✔️ | **Ready‑to‑run migrations** – 12 migration files covering schema evolution from the initial model to the final version. |

---  

## Tech Stack  

| Layer | Technology |
|-------|------------|
| **Backend** | Python 3.9+, Django 4.x |
| **Database** | SQLite (default) – can be swapped for PostgreSQL, MySQL, etc. |
| **Frontend** | Django templates + Bootstrap (optional) |
| **Blockchain** | Custom lightweight implementation in `myapp/blockchain.py` |
| **Version Control** | Git (GitHub) |

---  

## Installation  

> **Prerequisites**  
> * Python 3.9 or newer  
> * Git  
> * (Optional) virtualenv or conda for isolated environments  

```bash
# 1️⃣ Clone the repository
git clone https://github.com/your-username/register_login_django.git
cd register_login_django

# 2️⃣ Create and activate a virtual environment
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate

# 3️⃣ Install dependencies
pip install --upgrade pip
pip install -r requirements.txt   # (create this file if not present: Django==4.*)

# 4️⃣ Apply migrations
python manage.py migrate

# 5️⃣ Create a superuser (admin access)
python manage.py createsuperuser
# Follow the prompts – use a strong password

# 6️⃣ Run the development server
python manage.py runserver
```

The site will be available at `http://127.0.0.1:8000/`.  
Visit `/admin/` to log in with the superuser credentials and explore the admin UI.

---  

## Usage  

### 1. Register & Login  

* Navigate to `/register/` (or the URL you configure) to