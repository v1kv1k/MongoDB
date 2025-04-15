# Express MongoDB Docker Application

A simple Todo API built with Express.js and MongoDB, containerized with Docker.

## Features

- RESTful API for managing todos
- MongoDB integration
- Docker and Docker Compose configuration
- Hot-reloading for development

## Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/express-mongodb-docker.git
cd express-mongodb-docker
```

### 2. Start the application

```bash
docker compose up
```

This will:
- Build the Docker image for the Express application
- Start the Express API container
- Start the MongoDB container
- Connect the Express app to MongoDB
- Enable hot-reloading for development

### 3. Access the application

The API will be available at:
- http://localhost:3000

API Endpoints:
- GET / - Welcome message
- GET /todos - Get all todos
- POST /todos - Create a new todo
- PUT /todos/:id - Update a todo
- DELETE /todos/:id - Delete a todo

Example POST request to create a todo:
```bash
curl -X POST http://localhost:3000/todos \
  -H "Content-Type: application/json" \
  -d '{"text": "Learn Docker"}'
```

### 4. Development

Any changes made to the code will be automatically reflected in the running application thanks to the volume configuration in docker-compose.yml.

### 5. Stop the application

```bash
docker-compose down
```

To remove all data (including the MongoDB volume):

```bash
docker-compose down -v
``` #   M o n g o D B  
 