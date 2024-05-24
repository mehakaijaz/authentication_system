# Authentication System

## Overview

This project is an authentication system built with Django for the backend and JavaScript, HTML, and CSS for the frontend. It includes user registration, login, and logout functionalities. The system also has protected routes that only authenticated users can access.

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [File Structure](#file-structure)
5. [API Endpoints](#api-endpoints)
   
## Features

- User registration
- User login
- User logout
- Password hashing for secure storage
- Protected routes
- Session management

## Requirements

- Python 3.x
- Django 3.x
- MySQL (database for development)

### Backend

1. **Install backend dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

2. **Apply migrations**:
    ```sh
    python manage.py migrate
    ```

3. **Create a superuser**:
    ```sh
    python manage.py createsuperuser
    ```

4. **Run the development server**:
    ```sh
    python manage.py runserver
    ```

## Usage

1. Open your browser and go to `http://localhost:8000` to access the backend.
2. Register a new user or log in with an existing user account.
3. Access the protected routes by logging in.

## File Structure

```
auth-system/
│
├── backend/
│   ├── authenticationsystem/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   │   └── ...
│   ├── account/
│   │   ├── migrations/
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   └── ...
│   ├── manage.py
│   └── ...
│
├── new
├── README.md
└── requirements.txt
```

## API Endpoints

- **POST /api/register/**: Register a new user
- **POST /api/login/**: Login an existing user
- **POST /api/logout/**: Logout the current user
- **GET /api/profile/**: Get the profile of the logged-in user (protected route)
