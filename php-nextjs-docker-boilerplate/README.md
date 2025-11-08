# 🚀 PHP 8.4 + Next.js 15 Boilerplate with Docker

A modern full-stack boilerplate featuring **PHP 8.4** (API/backend) and **Next.js 15** (frontend) using **Docker** for streamlined local development and deployment.

---

## 📦 Features

- PHP 8.4 environment with Composer
- Next.js 15 with App Router support
- Docker-based development environment
- Hot-reloading for both frontend and backend
- Nginx reverse proxy
- Shared `.env` configuration for environment variables

---

## 📁 Directory Structure

```
project-root/
├── backend/
│   └── Dockerfile
├── frontend/
│   └── Dockerfile
├── nginx/
│   └── default.conf
├── docker-compose.yml
├── .env
└── README.md
```

---

## ⚙️ Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- Node.js (for local builds and linting if needed)

---

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/bhupeshdeveloper/php-nextjs-docker-boilerplate.git
cd php-nextjs-docker-boilerplate
```

### 2. Configure Environment

Copy `.env.example` to `.env` and adjust values if needed.

```bash
cp .env.example .env
```

### 3. Build and Start Containers

```bash
docker-compose up --build
```

This will start:

- PHP 8.4 container on port `9000`
- Next.js frontend on port `3000`
- Nginx proxy on port `80` (or configured value)

### 4. Access the App

- Frontend: [http://localhost](http://localhost)
- Backend API (example): [http://localhost/api](http://localhost/api)

---

## 🧪 Development

- Changes to the PHP backend auto-reload via `php-fpm`
- Next.js supports hot module reloading

```bash
# Access PHP container
docker exec -it php_container_name bash

# Access Next.js container
docker exec -it next_container_name bash
```

---

## 🧼 Common Commands

```bash
# Stop containers
docker-compose down

# Rebuild containers
docker-compose up --build

# Install PHP dependencies
docker exec php_container_name composer install

# Install JS dependencies
docker exec next_container_name npm install
```

---

## 📤 Deployment

For production setup, you may:

- Use a multistage Docker build
- Add SSL/TLS support with Let's Encrypt
- Use a production-ready web server configuration

---

## 📚 Stack Versions

| Tech        | Version    |
|-------------|------------|
| PHP         | 8.4        |
| Next.js     | 15         |
| Node.js     | 18+        |
| Docker      | 20+        |
| Nginx       | Latest     |

---

## 🙌 Contributing

Pull requests and issues are welcome! Please fork the repo and create a new branch.

---

## 📄 License

MIT © Bhupesh Kushwaha

---

## 🏷️ Tags

```
php, nextjs, docker, fullstack, boilerplate, dev-environment, php8, nextjs15, nginx
```

---

Let me know if you’d like me to generate the `docker-compose.yml` file or Dockerfiles for this project!