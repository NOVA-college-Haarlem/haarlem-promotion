# Haarlem Promotion

This repository contains a WordPress installation configured with Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

### Start the application

```bash
docker-compose up -d
```

This will start:
- WordPress on [http://localhost](http://localhost)
- MariaDB database (internal)

### Stop the application

```bash
docker-compose down
```

### Stop and remove volumes (clean slate)

```bash
docker-compose down -v
```

### View logs

```bash
docker-compose logs -f
```

