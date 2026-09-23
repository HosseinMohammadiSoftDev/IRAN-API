# IRAN-API

A lightweight RESTful API built with PHP for managing Iranian provinces and cities.

## Features

* RESTful API
* JWT Authentication
* Role & Province-based Authorization
* Province & City Management
* API Versioning
* MySQL / PDO
* File-based Caching
* Composer

## Architecture

The project follows a **Layered Architecture** with separation of HTTP, business logic, and infrastructure responsibilities.

```text
IRAN-API
│
├── api/                 # HTTP API endpoints
│   └── v1/
│
├── app/
│   ├── Services/        # Business logic
│   ├── Utilities/       # Shared infrastructure
│   └── iran.php         # Database / application configuration
│
├── vendor/              # Composer dependencies
│
├── composer.json
└── loader.php           # Application bootstrap
```

### Request Flow

```text
Client
  │
  ▼
API Endpoint
  │
  ▼
Authentication / Authorization
  │
  ▼
Service Layer
  │
  ▼
PDO / MySQL
  │
  ▼
Response
```

The **Service Layer** contains business logic and keeps the API endpoints focused on handling HTTP requests.

The **Utility Layer** provides reusable infrastructure such as response formatting and caching.

## Technology Stack

* PHP
* MySQL
* PDO
* Composer
* JWT
* PSR-4 Autoloading

## Installation

```bash
git clone https://github.com/HosseinMohammadiSoftDev/IRAN-API.git
cd IRAN-API

composer install
php -S localhost:8000
```

API:

```text
http://localhost:8000/api/v1/
```

## Project Status

This project is currently under development and is intended to evolve into a modular PHP API for Iranian geographic data and related services.

## License

MIT
