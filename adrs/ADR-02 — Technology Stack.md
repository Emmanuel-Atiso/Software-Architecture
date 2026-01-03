# ADR-002: Web-Based Technology Stack (PHP and MySQL)

## Status
Accepted

## Context
The Complaint Management System (CMS) proof of concept requires a stable, widely supported technology stack that enables rapid development, clear architectural layering, and easy deployment. The stack must support role-based access, structured complaint data, and integration with a relational database.

## Decision
The CMS is implemented using a web-based technology stack consisting of:
- A PHP-based backend application implementing business logic and complaint workflows
- A relational database (MySQL or MariaDB) for persistent data storage
- A web-based user interface built using standard web technologies (HTML, CSS, JavaScript)
- HTTP/HTTPS for communication between the user interface and backend services

The backend follows a layered structure, separating presentation, application, and data access responsibilities.

## Alternatives Considered
- Node.js with Express: Rejected to avoid introducing an additional runtime and to keep the implementation aligned with PHP tooling.
- Java with Spring Boot: Rejected due to higher development and configuration overhead for a proof of concept.
- Python with Django: Rejected to maintain consistency with the selected PHP ecosystem.

## Consequences
This technology stack supports rapid prototyping while remaining close to industry-standard web application architectures. PHP integrates well with MySQL and supports clear separation of concerns through a layered structure. While not as horizontally scalable as microservice-based stacks, this approach is appropriate for a proof of concept and can be evolved in the future.
