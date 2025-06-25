# Late Show API

A **Flask REST API** for managing Late Show Episodes, Guests, and Appearances.

## Setup

1. Clone the repository at:

   ```bash
   https://github.com/Jjumaaa/Phase-4-Code-Challenge-Two-Late-Show-API.git
   Then, cd late-show-api
   ```
2. Install dependencies:

   ```bash
   pipenv install
   pipenv shell
   ```

## Environment Variables

Create a `.env` file:

```bash
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=super-secret-key
DATABASE_URL=sqlite:///app.db
```

## Dependencies

Install them with =pipenv "The dependency you want"

* flask
* flask-sqlalchemy
* flask-migrate
* flask-jwt-extended
* psycopg2-binary
* pipenv
* shell
* faker
* alembic
* flask-cors
* sqlalchemy
* serializer
* sqlalchemy-serializer
* flask-bcrypt
* flask-restful

## Database Migrations

```bash
alembic init alembic
alembic revision --autogenerate -m "Make tables"
alembic upgrade head
```

## Seeding the Database

```bash
python seed.py
```

## Run the Server

```bash
python app.py
```

## Authentication Flow

* **Register:** `POST /register`
* **Login:** `POST /login` (returns a JWT token)

Use the returned `token` in requests:

```
Authorization: Bearer <your_jwt_token_here>
```

## Available Routes

* `GET /episodes`
* `GET /episodes/<id>`
* `GET /guests`
* `POST /appearances` *(Requires JWT Auth)*

## Postman Usage Guide

Import into Postman and test endpoints for Registration, Login, Viewing Episodes, Viewing Guests, and Creating Appearances.

## GitHub Repository

[https://github.com/Jjumaaa/Phase-4-Code-Challenge-Two-Late-Show-API.git](https://github.com/Jjumaaa/Phase-4-Code-Challenge-Two-Late-Show-API.git)

## Screenshots
   # Appearances.png
   ![alt text](Screenshots/Appearances.png)

   # AppearancesAfterBearerTokeninput.png
   ![alt text](Screenshots/AppearancesAfterBearerTokeninput.png)

   # Episodes.png
   ![alt text](Screenshots/Episodes.png)

   # EpisodesWithID.png
   ![alt text](Screenshots/EpisodesWithID.png)

   # Guests.png
   ![alt text](Screenshots/Guests.png)

   # Login.png
   ![alt text](Screenshots/Login.png)

   # RegisterUsers.png
   ![alt text](Screenshots/RegisterUsers.png)