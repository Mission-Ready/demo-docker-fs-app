# Dockerized Application

This project is a web application consisting of a frontend, backend, and a MySQL database, all containerized using Docker and managed with Docker Compose.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. **Build and start the containers:**

   ```bash
   docker-compose up --build
   ```

3. **Access the application:**

   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend API: [http://localhost:3001](http://localhost:3001)

## Services

- **frontend**: React app build vite Node.js and served via Nginx.
- **backend**: Node.js/Express application.
- **mysql**: MySQL database with persistent storage.

## Database Configuration

- **Host**: `mysql`
- **Port**: `3306`
- **Database**: `myappdb`
- **User**: `myuser`
- **Password**: `mypassword`

## Volumes

- `mysql-data`: Persists MySQL data between container restarts.

## Notes

- Ensure the `init.sql` script is present in the root directory to initialize the database on the first run.
- Environment variables are set in the docker-compose.yml file.

## Stopping the Application

To stop the application and remove containers, networks, and volumes, run:

```bash
docker-compose down
```