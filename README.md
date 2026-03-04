# Ecommerce

Full-stack ecommerce application built with Nuxt 4 (Vue 3) and Laravel, orchestrated with Docker Compose.

## Tech Stack

- **Frontend:** Nuxt 4, Vue 3, Pinia, Tailwind CSS
- **Backend:** Laravel (PHP)
- **Database:** MySQL
- **Reverse Proxy:** Nginx
- **Containerization:** Docker & Docker Compose

## Project Structure

```
├── ecommerce-frontend/   # Nuxt 4 frontend
├── ecommerce-backend/    # Laravel API backend
├── nginx/                # Nginx configuration
├── docker-compose.yml    # Development environment
└── docker-compose-prod.yml  # Production environment
```

## Getting Started

### Prerequisites

- Docker & Docker Compose

### Development

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd ecommerce
   ```

2. Copy environment files:
   ```bash
   cp ecommerce-backend/.env.example ecommerce-backend/.env
   ```

3. Start the services:
   ```bash
   docker compose up -d
   ```

4. Access the application:
   - **Frontend:** http://localhost:3000
   - **Backend API:** http://localhost:8000
   - **phpMyAdmin:** http://localhost:8001

### Production

```bash
docker compose -f docker-compose-prod.yml up -d
```

In production, Nginx serves the static frontend build and proxies API requests to the Laravel backend over ports 80/443.
