# Django Authentication App

## Overview
This is a Django-based authentication app that provides user registration, login, logout, and password reset functionality. It is designed to be easily integrated into any Django project.

## Features
- User registration with email verification
- Login and logout functionality
- Secure password hashing
- Password reset via email
- Django authentication backend integration
- Customizable user model
- API support (optional, using Django REST Framework)

## Requirements
- Python 3.x
- Django 4.x
- Django REST Framework (if API support is needed)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/mehdidinari/auth-app.git
   cd auth-django-app
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Apply migrations:
   ```bash
   python manage.py migrate
   ```

5. Create a superuser:
   ```bash
   python manage.py createsuperuser
   ```

6. Run the server:
   ```bash
   python manage.py runserver
   ```

## Usage
- Register a new user at `/register/`
- Login at `/login/`
- Logout at `/logout/`
- Reset password at `/password-reset/`
- Access the Django admin panel at `/admin/`

## API Endpoints (if using DRF)
- `POST /api/register/` - Register a new user
- `POST /api/login/` - Authenticate user and return token
- `POST /api/logout/` - Logout user
- `POST /api/password-reset/` - Send password reset email

## Configuration
Modify the `settings.py` file to customize authentication settings:
```python
AUTH_USER_MODEL = 'yourapp.CustomUser'
LOGIN_REDIRECT_URL = '/dashboard/'
LOGOUT_REDIRECT_URL = '/login/'
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a new branch (`feature-branch`)
3. Commit your changes
4. Push to the branch and submit a Pull Request

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For any issues, please open an issue on GitHub or contact [treshlol202@gmail.com].

