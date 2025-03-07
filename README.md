# Django Authentication System

A robust authentication system built with Django that provides user registration, login, password management, and profile functionality.

## Features

- 👤 User Authentication
  - Login with username/email
  - User registration
  - Password reset functionality
  - Change password option
- 👨‍💼 User Profile Management
- 📊 User Dashboard
- 🔒 Secure Authentication Flows
- 💅 Clean and Responsive UI

## Tech Stack

- Python 3.x
- Django 5.1.5
- SQLite (Development)
- PostgreSQL (Production)
- Whitenoise for static files
- HTML/CSS for frontend

## Installation

1. Clone the repository
```bash
git clone <repository-url>
cd auth_project_django
```

2. Create and activate virtual environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Apply migrations
```bash
python manage.py migrate
```

5. Create superuser
```bash
python manage.py createsuperuser
```

6. Run the development server
```bash
python manage.py runserver
```

## Usage

After starting the server, you can access:

- Homepage/Login: `http://127.0.0.1:8000/`
- Registration: `http://127.0.0.1:8000/signup/`
- Dashboard: `http://127.0.0.1:8000/dashboard/`
- Profile: `http://127.0.0.1:8000/profile/`
- Admin Interface: `http://127.0.0.1:8000/admin/`

## Project Structure
auth_project_django/
├── auth_project/
│ ├── accounts/ # Authentication app
│ │ ├── views.py # View logic
│ │ ├── urls.py # URL configurations
│ │ └── models.py # Data models
│ ├── templates/ # HTML templates
│ │ ├── login.html
│ │ ├── signup.html
│ │ ├── dashboard.html
│ │ ├── profile.html
│ │ └── ...
│ └── auth_project/ # Project settings
│ ├── settings.py
│ └── urls.py
└── manage.py
## Deployment

The project is configured for deployment on various platforms:

### Heroku
- Procfile included
- Whitenoise configured for static files
- Database configuration ready for PostgreSQL

### Other Platforms
- Configure `ALLOWED_HOSTS` in settings.py
- Set `DEBUG = False` in production
- Set up proper database credentials
- Configure email backend for password reset

## Security Features

- CSRF protection enabled
- Password validation rules
- Secure password reset flow
- Session management
- Protected views with login_required

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
