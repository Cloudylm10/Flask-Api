# Travel API with Flask and Docker

A RESTful API for managing travel destinations built with Flask, SQLAlchemy, and Docker.

## Features

- CRUD operations for travel destinations
- SQLite database with SQLAlchemy ORM
- Dockerized for easy deployment
- RESTful endpoints with JSON responses

## API Endpoints

| Method | Endpoint                | Description                          |
|--------|-------------------------|--------------------------------------|
| GET    | /                       | Welcome message                     |
| GET    | /destinations           | Get all destinations                |
| GET    | /destinations/<id>      | Get a specific destination          |
| POST   | /destinations           | Add a new destination               |
| PUT    | /destinations/<id>      | Update a destination                |
| DELETE | /destinations/<id>      | Delete a destination                |

## Prerequisites

- Docker
- Docker Compose
- Python 3.11 (if running locally without Docker)

## Getting Started

### With Docker (Recommended)

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/travel-api.git
   cd travel-api
Build and run the containers:

bash
docker-compose up --build
The API will be available at http://localhost:5000

Without Docker
Clone the repository:

bash
git clone https://github.com/yourusername/travel-api.git
cd travel-api
Create a virtual environment:

bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install dependencies:

bash
pip install -r requirements.txt
Run the application:

bash
flask run

API Usage Examples
Create a new destination
bash
curl -X POST -H "Content-Type: application/json" -d '{
    "destination": "Eiffel Tower",
    "country": "France",
    "rating": 4.8
}' http://localhost:5000/destinations
Get all destinations
bash
curl http://localhost:5000/destinations
Update a destination
bash
curl -X PUT -H "Content-Type: application/json" -d '{
    "rating": 4.9
}' http://localhost:5000/destinations/1
Delete a destination
bash
curl -X DELETE http://localhost:5000/destinations/1
Project Structure
text
travel-api/
├── .dockerignore
├── .gitignore
├── docker-compose.yml
├── Dockerfile
├── README.md
├── app.py
├── requirements.txt
└── travel.db
Technologies Used
Flask - Web framework

SQLAlchemy - ORM for database operations

Docker - Containerization

SQLite - Database
