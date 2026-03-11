# Haarlem Promotion

This repository contains a Docker compose file that will create a clean installation of the latest Wordpress version.

## Prerequisites

- Docker

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

## Troubleshooting

### Admin password lost

If you've lost your administrator password do the following: Open the database via phpMyAdmin (http://localhost:8080/). Select the `wordpress` database and run the following query in the tab "SQL":

```sql
UPDATE wp_users SET user_pass = MD5('MijnNieuwWachtwoord!') WHERE user_login = 'admin';
```

Now you should be able to login at http://localhost/wp-admin.
