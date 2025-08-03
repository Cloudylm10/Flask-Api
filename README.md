
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

2. Build and run the containers:
   ```bash
   docker-compose up --build
3. The API will be available at http://localhost:5000

### Without Docker 

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/travel-api.git
   cd travel-api
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
4. Run the application:
   ```bash
   flask run

## API Testing with Postman

### Collection Setup
1. Import our [Postman Collection](#) (link your collection if available)
2. Environment variables:
   - Set `base_url` to `http://localhost:5000`

### Request Examples

#### 1. Create Destination
- **Method**: POST
- **Endpoint**: `/destinations`
- **Headers**:
  - `Content-Type: application/json`
- **Body (raw JSON)**:
  ```json
  {
    "destination": "Eiffel Tower",
    "country": "France",
    "rating": 4.8
  }

- Success Response (201 Created):
  ```json
  {
   "id": 1,
   "destination": "Eiffel Tower",
   "country": "France",
   "rating": 4.8
  }

#### 2. Get All Destinations
- **Method**: GET
- **Endpoint**: `/destinations`
- Success Response (200 OK):
  ```json
  {
     "id": 1,
     "destination": "Eiffel Tower",
     "country": "France",
     "rating": 4.8
  }

#### 3. Update Destination
- **Method**: PUT
- **Endpoint**: `/destinations/1 (replace with actual ID)`
- **Headers**:
  - `Content-Type: application/json`
- **Body (raw JSON)**:
  ```json
  {
    "rating": 4.8
  }

- Success Response (201 Created):
  ```json
  {
     "id": 1,
     "destination": "Eiffel Tower",
     "country": "France",
     "rating": 4.9
  }

#### 4. DELETE Destination
- **Method**: DELETE
- **Endpoint**: `/destinations/1 (replace with actual ID)`

- Success Response (201 Created):
  ```json
  {
    "message": "Destination was deleted!"
  }

## Project Structure

```
travel-api/
├── .dockerignore       # Files to exclude from Docker builds
├── .gitignore         # Files to exclude from version control
├── docker-compose.yml # Docker container orchestration
├── Dockerfile         # Docker image configuration
├── README.md          # Project documentation
├── app.py             # Main application code
├── requirements.txt   # Python dependencies
└── travel.db          # SQLite database (ignored in .gitignore)
```
## Technologies Used

- Flask - Web framework
- SQLAlchemy - ORM for database operations
- Docker - Containerization
- SQLite - Database
- Postman - API Testing

## License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgements

- Flask and SQLAlchemy teams
- Docker community
- All open source contributors


## Initial Git Setup

Follow the steps below to initialize a Git repository and push your project to GitHub.

```bash
# Step 1: Initialize Git Repository
git init

# Step 2: Add Files and Make Initial Commit
git add .
git commit -m "Initial commit with Flask Travel API and Docker setup"

# Step 3: Connect to GitHub and Push
git remote add origin https://github.com/yourusername/travel-api.git
git branch -M main
git push -u origin main

##Python Requirements

You don't need a separate `requirements.txt` file. Just install these Python dependencies:

```bash
pip install Flask==2.3.2 Flask-SQLAlchemy==3.0.3









   


