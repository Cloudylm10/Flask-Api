# Travel API with Flask and Docker

A RESTful API for managing travel destinations built with Flask, SQLAlchemy, and Docker.

## Features
- CRUD operations for travel destinations
- SQLite database with SQLAlchemy ORM  
- Dockerized for easy deployment
- RESTful endpoints with JSON responses

## API Endpoints

| Method | Endpoint                | Description                     |
|--------|-------------------------|---------------------------------|
| GET    | `/`                     | Welcome message                |
| GET    | `/destinations`         | Get all destinations           |
| GET    | `/destinations/<id>`    | Get a specific destination     |
| POST   | `/destinations`         | Add a new destination          |
| PUT    | `/destinations/<id>`    | Update a destination           |
| DELETE | `/destinations/<id>`    | Delete a destination           |

## Prerequisites
- Docker
- Docker Compose
- Python 3.11 (if running locally without Docker)

## Getting Started

### With Docker (Recommended)
```bash
git clone https://github.com/yourusername/travel-api.git
cd travel-api
docker-compose up --build
The API will be available at http://localhost:5000

### Local Development (Without Docker)

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/travel-api.git
cd travel-api

