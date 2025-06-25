##


## Project Overview

This project sets up a Docker Compose-based system with three Docker containers:

- **Nginx Reverse Proxy** container that routes incoming HTTP requests based on URL path prefixes.
- **Service 1** container running a Golang application.
- **Service 2** container running a Python application.

The reverse proxy routes requests as follows:

- Requests to `/service1` are forwarded to the Golang backend (Service 1).
- Requests to `/service2` are forwarded to the Python backend (Service 2).

All services are accessible via a single port (e.g., `localhost:8080`).

---

## Project Structure

.
├── docker-compose.yml
├── nginx
│ ├── Dockerfile
│ └── nginx.conf
├── service_1
│ └── Dockerfile
├── service_2
│ └── Dockerfile
└── README.md

yaml
Copy
Edit

---

## Prerequisites

- Docker installed ([Get Docker](https://docs.docker.com/get-docker/))
- Docker Compose installed ([Install Docker Compose](https://docs.docker.com/compose/install/))
- Git installed ([Get Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git))

---

## Setup and Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/kirankumar673/dpdzero-assignment/blob/main/docker-compose.yml
   
Build and start all services

docker-compose up -- build



Open your browser or API client and test the endpoints:

http://localhost:8080/service1/ping → Routes to the Golang service.

http://localhost:8080/service1/hello

http://localhost:8080/service2/ping → Routes to the Python service.

http://localhost:8080/service2/hello
