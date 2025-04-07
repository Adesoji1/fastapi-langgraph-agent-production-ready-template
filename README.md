# FastAPI LangGraph Agent Template

A production-ready FastAPI template for building AI agent applications with LangGraph integration. This template provides a robust foundation for building scalable, secure, and maintainable AI agent services.

## 🌟 Features

- **Production-Ready Architecture**
  - FastAPI for high-performance async API endpoints
  - LangGraph integration for AI agent workflows
  - Langfuse for LLM observability and monitoring
  - Structured logging with environment-specific formatting
  - Rate limiting with configurable rules
  - PostgreSQL for data persistence
  - Docker and Docker Compose support
  - Prometheus metrics and Grafana dashboards for monitoring

- **Security**
  - JWT-based authentication
  - Session management
  - Input sanitization
  - CORS configuration
  - Rate limiting protection

- **Developer Experience**
  - Environment-specific configuration
  - Comprehensive logging system
  - Clear project structure
  - Type hints throughout
  - Easy local development setup

## 🚀 Quick Start

### Prerequisites

- Python 3.13+
- PostgreSQL
- Docker and Docker Compose (optional)

### Environment Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd <project-directory>
```

2. Create and activate a virtual environment:
```bash
uv sync
```

3. Copy the example environment file:
```bash
cp .env.example .env.[development|staging|production] # e.g. .env.development
```

4. Update the `.env` file with your configuration (see `.env.example` for reference)

### Running the Application

#### Local Development

1. Install dependencies:
```bash
uv sync
```

2. Run the application:
```bash
make [dev|staging|production] # e.g. make dev
```

1. Go to Swagger UI:
```bash
http://localhost:8000/docs
```

#### Using Docker

1. Build and run with Docker Compose:
```bash
make docker-build-env ENV=[development|staging|production] # e.g. make docker-build-env ENV=development
make docker-run-env ENV=[development|staging|production] # e.g. make docker-run-env ENV=development
```

2. Access the monitoring stack:
```bash
# Prometheus metrics
http://localhost:9090

# Grafana dashboards
http://localhost:3000
Default credentials:
- Username: admin
- Password: admin
```

The Docker setup includes:
- FastAPI application
- PostgreSQL database
- Prometheus for metrics collection
- Grafana for metrics visualization
- Pre-configured dashboards for:
  - API performance metrics
  - Rate limiting statistics
  - Database performance
  - System resource usage

## 🔧 Configuration

The application uses a flexible configuration system with environment-specific settings:

- `.env.development`