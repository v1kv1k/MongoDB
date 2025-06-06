# 🐳 Express MongoDB Docker Application

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)

A modern Todo API built with Express.js and MongoDB, containerized with Docker for easy deployment and development.

## ✨ Features

- 🔄 **RESTful API** for managing todos
- 🗄️ **MongoDB integration** for data persistence
- 🐳 **Docker and Docker Compose** configuration for easy setup
- 🔥 **Hot-reloading** for development efficiency
- 🔒 **Containerized environment** for consistent development and production

## 🛠️ Technologies

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Containerization**: Docker, Docker Compose
- **Development Tools**: Nodemon for hot-reloading

## 📋 Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/v1kv1k/MongoDB.git
cd MongoDB
```

### 2️⃣ Start the application

```bash
docker compose up
```

This command will:
- 🏗️ Build the Docker image for the Express application
- 🚀 Start the Express API container
- 🗄️ Start the MongoDB container
- 🔄 Connect the Express app to MongoDB
- 🔥 Enable hot-reloading for development

### 3️⃣ Access the application

The API will be available at:
- 🌐 http://localhost:3000

## 📚 API Documentation

### Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | /        | Welcome message |
| GET    | /todos   | Get all todos |
| POST   | /todos   | Create a new todo |
| PUT    | /todos/:id | Update a todo |
| DELETE | /todos/:id | Delete a todo |

### Example Requests

#### Create a new todo

```bash
curl -X POST http://localhost:3000/todos \
  -H "Content-Type: application/json" \
  -d '{"text": "Learn Docker"}'
```

#### Get all todos

```bash
curl -X GET http://localhost:3000/todos
```

## 🧑‍💻 Development

Any changes made to the code will be automatically reflected in the running application thanks to the volume configuration in docker-compose.yml.

## 📁 Project Structure

```
.
├── app.js              # Express application
├── package.json        # Node.js dependencies
├── Dockerfile          # Docker image configuration
├── docker-compose.yml  # Docker Compose services setup
├── .gitignore          # Git ignore rules
└── README.md           # Project documentation
```

## 🛑 Stop the application

```bash
docker compose down
```

To remove all data (including the MongoDB volume):

```bash
docker compose down -v
```

## 📦 Docker Configuration

### Dockerfile

The project uses a Dockerfile that:
- Uses the latest LTS version of Node.js
- Sets up a working directory in /app
- Installs dependencies
- Exposes port 3000
- Runs the application

### Docker Compose

The docker-compose.yml file includes:
- Express application service
- MongoDB service
- Volume mappings for persistent data
- Environment variables for configuration
- Port mappings for accessibility

## 📝 License

This project is open source and available under the [MIT License](LICENSE).
