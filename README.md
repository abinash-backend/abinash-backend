# Abinash Nayak

**Backend Engineer | Java | Spring Boot | System Design**

Based in India | MCA – Biju Patnaik University of Technology (BPUT), 2024

---

## Introduction

Backend engineer passionate about designing and building scalable backend systems. Experienced in developing robust REST APIs, implementing secure authentication mechanisms, architecting production-ready systems, and enforcing clear domain boundaries through modular architecture. I specialize in clean code, system design principles, and translating business requirements into maintainable backend solutions.

My portfolio demonstrates practical expertise across multiple domains: travel booking systems with payment integration, workflow execution platforms with task orchestration, and complex authentication/authorization patterns. Each project follows production-oriented practices including containerization, API documentation, and comprehensive testing strategies.

---

## About Me

I specialize in backend architecture and API development with a strong emphasis on:

- **Backend System Design**: Building scalable, maintainable systems following clean architecture principles and modular monolith patterns
- **REST API Development**: Designing RESTful services with proper error handling, validation, and OpenAPI documentation
- **Security**: Implementing authentication and authorization using JWT, Spring Security, and role-based access control
- **Database Design**: Architecting relational database schemas with proper indexing, query optimization, and transactional consistency
- **Production Readiness**: Writing code that's deployable, monitorable, and maintainable with Docker containerization and CI/CD pipelines
- **Domain-Driven Design**: Separating business concerns into explicit modules with clear ownership boundaries

My approach combines theoretical understanding of system design with practical implementation experience using industry-standard frameworks and tools.

---

## Current Projects

### 1. TripOps | Travel Booking & Inventory Management Service
**Repository**: [tripops-backend](https://github.com/abinash-backend/tripops-backend)

A production-grade Spring Boot backend for travel booking workflows, package inventory management, secure payment processing, and operational API flows. Implemented as a modular monolith with explicit domain boundaries.

**Key Features**:
- Stateless JWT authentication with RBAC (USER, ADMIN roles)
- Package catalog management with inventory tracking and capacity constraints
- Complete booking workflow with ownership-scoped access control
- Payment integration with Razorpay for secure transaction handling
- Redis-backed caching for high-read package endpoints
- Structured error handling and OpenAPI/Swagger documentation
- Docker and Docker Compose configuration for containerized deployment

**Architecture Highlights**:
- **Modular Monolith**: Single deployable unit with clear domain modules (auth, user, packages, booking, payment)
- **Layered Design**: Controller → Service → Repository → PostgreSQL
- **Caching Strategy**: Redis for package reads with TTL-based invalidation on mutations
- **API Documentation**: OpenAPI/Swagger UI for interactive testing and integration
- **Transactional Consistency**: Service-layer transaction boundaries with read-only query optimization

**Tech Stack**:
- Java 21 | Spring Boot 3.1.4 | Spring Security | JWT
- PostgreSQL | Redis | Hibernate/JPA
- Maven | Docker | GitHub Actions
- OpenAPI/Swagger | JUnit 5, Mockito, Spring Security Test

**Domains**:
| Module | Responsibility |
|--------|---|
| `auth` | Login, JWT issuance, authenticated principal resolution |
| `user` | User registration, admin creation, role assignment |
| `packages` | Package catalog, inventory lifecycle, cached reads |
| `booking` | Booking creation, retrieval, ownership enforcement |
| `payment` | Payment records, Razorpay integration, booking confirmation |
| `common` | Security, OpenAPI, cache config, exception handling |

---

### 2. Nexus | Workflow Execution Platform
**Repository**: [nexus-backend](https://github.com/abinash-backend/nexus-backend)

A backend platform for workflow execution, task orchestration, and execution lifecycle tracking. Designed for accountability and predictable state handling with clear domain separation.

**Key Features**:
- User-scoped task creation and retrieval with ownership enforcement
- Execution logging with per-task, per-day tracking and idempotency guards
- Composite database constraints preventing duplicate same-day execution entries
- Streak and consistency calculations from persisted execution history
- Leaderboard-style user aggregation for consistency scoring
- OpenAPI documentation for API consumers
- Containerized runtime with Docker and Docker Compose
- Actuator-backed health exposure for operational monitoring

**Architecture Highlights**:
- **Modular Monolith**: Domain-driven module separation with clear boundaries
- **Workflow Model**: Task ownership with execution traceability and audit trails
- **Consistency**: Single-database transactional model with application-level validation
- **Layered Flow**: Controller → Service → Repository → PostgreSQL
- **API Documentation**: Springdoc OpenAPI with Swagger UI and bearer auth support

**Tech Stack**:
- Java 17 | Spring Boot 3.5.12 | Spring Security | JWT
- PostgreSQL 15 | Spring Data JPA
- Maven | Docker | GitHub Actions
- OpenAPI/Swagger | JUnit 5, Mockito, Spring Security Test

**Domains**:
| Module | Responsibility |
|--------|---|
| `auth` | Registration, login, password hashing, JWT issuance |
| `task` | Task creation, retrieval, filters, streak computation, leaderboard |
| `execution` | Execution logging, history tracking, idempotency constraints |
| `common` | Security, OpenAPI, exception handling, utilities |
| `system` | Health and service availability endpoints |

---

## Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java-17%20%2B%2021-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.4%20%2B%203.5.12-6DB33F?style=flat&logo=spring-boot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-JWT%20%2B%20RBAC-6DB33F?style=flat&logo=spring&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-OpenAPI%2FSwagger-FF6B6B?style=flat&logo=api&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-JJWT%200.11.5-000000?style=flat&logo=JSON%20web%20tokens&logoColor=white)

### Database & Cache
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15%2B-336791?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-Spring%20Cache-DC382D?style=flat&logo=redis&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-ORM-59666C?style=flat&logo=hibernate&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-Spring%20Data-007396?style=flat&logo=java&logoColor=white)

### DevOps & Infrastructure
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-Version%20Control-F05032?style=flat&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=flat&logo=github-actions&logoColor=white)
![Maven](https://img.shields.io/badge/Build-Maven-C71A36?style=flat&logo=apachemaven&logoColor=white)

### Testing & Quality
![JUnit 5](https://img.shields.io/badge/Testing-JUnit%205-25A217?style=flat&logo=junit5&logoColor=white)
![Mockito](https://img.shields.io/badge/Mocking-Mockito-FF6B35?style=flat&logo=mockito&logoColor=white)
![MockMvc](https://img.shields.io/badge/Integration-MockMvc-6DB33F?style=flat&logo=spring&logoColor=white)

### Architecture & Design
- **Modular Monolith**: Clear domain boundaries with single deployable unit
- **Domain-Driven Design (DDD)**: Explicit module ownership and responsibility
- **Clean Architecture**: Layered separation of concerns (Controller → Service → Repository)
- **SOLID Principles**: Single responsibility, dependency inversion, interface segregation
- **System Design Patterns**: Caching strategies, transaction management, error handling
- **Microservices-Ready**: Clear seams for future service extraction if scaling demands require

---

## Key Architectural Patterns & Decisions

### Modular Monolith Approach

Both projects follow a modular monolith architecture, intentionally choosing a single deployable unit while enforcing clear domain boundaries. This pattern provides:

- **Operational Simplicity**: One runtime, straightforward local development, transactional consistency
- **Maintainability**: Clear module ownership makes navigation intuitive and lowers extraction cost
- **Flexibility**: Designed with seams for future service extraction without claiming premature distribution
- **Coordination**: Low overhead for cross-domain interactions within single process
- **Consistency**: Relational database transactions ensure correctness across modules

### Security Model

- **Stateless Authentication**: JWT bearer tokens validated per request with no sessions
- **RBAC**: Role-based access control for USER and ADMIN paths
- **Password Security**: BCrypt hashing for password storage
- **Method-Level Authorization**: `@PreAuthorize` annotations for fine-grained access control
- **Error Normalization**: Consistent JSON error responses for unauthorized/forbidden scenarios

### Caching Strategy (TripOps)

Redis provides a backing store for Spring Cache:
- Package reads cached with 10-30 minute TTLs
- Cache invalidation coupled to package mutations
- JSON serialization for value storage
- Null values excluded from cache

### Database Consistency

- **Single-Database Model**: All business transactions within one relational boundary
- **Transaction Boundaries**: Service-layer `@Transactional` annotations
- **Query Optimization**: `readOnly = true` for non-mutating paths
- **Open-in-View Disabled**: Explicit persistence behavior prevents lazy-loading surprises
- **Constraint Enforcement**: Database-level uniqueness constraints (e.g., duplicate execution prevention)

---

## API Documentation & Testing

Both projects expose OpenAPI/Swagger for interactive API discovery:

**TripOps**:
- Swagger UI: `http://localhost:8080/swagger-ui/index.html`
- OpenAPI JSON: `http://localhost:8080/v3/api-docs`

**Nexus**:
- Swagger UI: `http://localhost:8080/swagger-ui.html`
- OpenAPI JSON: `http://localhost:8080/v3/api-docs`

Comprehensive test coverage includes:
- Unit tests for business logic
- Controller integration tests with MockMvc
- Security and authentication tests
- Spring Security test utilities for endpoint authorization

---

## Deployment & CI/CD

### Docker Containerization

Both projects include:
- **Multi-Stage Builds**: Optimized image sizes with separate build and runtime stages
- **Docker Compose**: Local development stacks with PostgreSQL, Redis (TripOps), and the backend
- **Health Checks**: Container readiness validation before accepting traffic
- **Non-Root Runtime**: Security-hardened container user configuration

### CI/CD Pipelines

- **GitHub Actions**: Automated Maven builds on push/PR
- **Test Execution**: Mandatory test runs before merge
- **Docker Publishing**: Automated image builds after successful test runs
- **Deployment Hooks**: Integration with Render or similar platforms

---

## Production Considerations

Both projects are designed with production readiness in mind:

- **Externalized Configuration**: Environment-driven secrets and settings
- **Schema Migrations**: Ready for Flyway/Liquibase integration
- **Observability Readiness**: Structured logging, health endpoints, actuator support
- **Rate Limiting**: Foundation for implementing request throttling
- **Audit Trails**: Comprehensive execution and booking history for compliance

---

## Learning Focus

Currently focused on:

- Advanced system design and architectural patterns for scale
- Distributed systems concepts and eventual consistency models
- Production-ready Spring Boot application development at scale
- Cloud deployment patterns and infrastructure as code
- API design best practices, versioning strategies, and backward compatibility
- Event-driven architecture and async workflow patterns
- Observability: structured logging, tracing, and metrics collection

---

## GitHub Repositories

- **TripOps Backend**: [github.com/abinash-backend/tripops-backend](https://github.com/abinash-backend/tripops-backend)
- **Nexus Backend**: [github.com/abinash-backend/nexus-backend](https://github.com/abinash-backend/nexus-backend)
- **Profile**: [github.com/abinash-backend/abinash-backend](https://github.com/abinash-backend/abinash-backend)

---

## GitHub Stats

![Abinash's GitHub Stats](https://github-readme-stats.vercel.app/api?username=abinash-backend&show_icons=true&theme=default&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=abinash-backend&layout=compact&theme=default&hide_border=true)

---

## Connect

- **LinkedIn**: [linkedin.com/in/abinash-nayak-9079b221b](https://www.linkedin.com/in/abinash-nayak-9079b221b?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)
- **Portfolio**: [abinash-nayak-portfolio.netlify.app](https://abinash-nayak-portfolio.netlify.app)
- **Email**: [abinash.tech.ai@gmail.com](mailto:abinash.tech.ai@gmail.com)

---

*Last updated: 2026-05-22*
