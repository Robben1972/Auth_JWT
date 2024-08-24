Here's a `README.md` template you can use for your GitHub repository:

```markdown
# Django REST Framework JWT Authentication

This project is a simple Django REST API that provides user registration and login functionality using JWT (JSON Web Token) for authentication.

## Features

- **User Registration**: Users can sign up and receive an authentication token.
- **User Login**: Users can log in with their credentials and receive a token.
- **Token Authentication**: Secured API endpoints using session and token authentication.

## Endpoints

### 1. User Signup

**URL**: `/api/signup/`  
**Method**: `POST`  
**Request Body**:
```json
{
  "username": "your_username",
  "password": "your_password",
  "email": "your_email@example.com"
}
```

**Response**:
- **200 OK**: Returns a token and user details.
- **400 Bad Request**: Returns validation errors.

### 2. User Login

**URL**: `/api/login/`  
**Method**: `POST`  
**Request Body**:
```json
{
  "username": "your_username",
  "password": "your_password"
}
```

**Response**:
- **200 OK**: Returns a token and user details.
- **404 Not Found**: Returns "missing user" if the credentials are invalid.

### 3. Test Token

**URL**: `/api/test-token/`  
**Method**: `GET`  
**Authentication**: Requires token authentication.

**Response**:
- **200 OK**: Returns "passed!" if the token is valid.

## Setup and Installation

### 1. Clone the Repository

```bash
git git@github.com:Robben1972/Auth_JWT.git
cd repo-name
```

### 2. Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Migrations

```bash
python manage.py migrate
```

### 6. Run the Development Server

```bash
python manage.py runserver
```

## Testing the Endpoints

You can test the API endpoints using tools like [Postman](https://www.postman.com/) or [cURL](https://curl.se/), or just use test.rest file.
